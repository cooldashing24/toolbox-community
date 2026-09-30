# Privacy Architecture & Client-Side Execution Model

> **Author**: Toolbox Engineering Team (`contact@toolbox.vishnudigital.com`)  
> **Published**: 2026  
> **Platform**: [https://toolbox.vishnudigital.com](https://toolbox.vishnudigital.com)  
> **Companion Blog**: [https://blog.toolbox.vishnudigital.com](https://blog.toolbox.vishnudigital.com)

---

## Executive Summary

Software engineers frequently need to format JSON payloads, inspect JSON Web Tokens (JWTs), convert cURL commands into application code, test regular expressions, and generate cryptographic keys. However, modern corporate security policies under **SOC 2 Type II, HIPAA, GDPR, PCI-DSS, and ISO/IEC 27001** explicitly forbid uploading sensitive data—such as production API tokens, customer PII, database connection strings, and proprietary schemas—to third-party web services that log requests in remote server access logs.

**Toolbox** was architected from day one as a **global, air-gapped, zero-telemetry web workbench**. Delivered instantly worldwide via global edge networks, every calculation, AST traversal, regular expression evaluation, and cryptographic operation executes 100% within the user's browser process memory (RAM).

```
┌────────────────────────────────────────────────────────────────────────┐
│             GLOBAL WEB DELIVERY (https://toolbox.vishnudigital.com)    │
│                                                                        │
│   ┌────────────────────────────────────────────────────────────────┐   │
│   │                 In-Browser Process Memory Sandbox              │   │
│   │                                                                │   │
│   │   [ Raw Input ]  ──►  [ WebCrypto / AST / Canvas ]             │   │
│   │   (JWT, JSON, PII)           │                                 │   │
│   │                              ▼                                 │   │
│   │                      [ Clean Output ]                          │   │
│   │                                                                │   │
│   │   * Ephemeral JS Heap                                          │   │
│   │   * Cleared on Tab Close                                       │   │
│   │   * Zero Persistent Storage Logging                            │   │
│   └────────────────────────────────────────────────────────────────┘   │
└────────────────────────────────────────────────────────────────────────┘
                                    │
                         ✖  NO NETWORK TRANSMISSION
                                    │
                                    ▼
                     ┌─────────────────────────────┐
                     │   Remote Backend Servers    │
                     │    (Zero Payload Access)    │
                     └─────────────────────────────┘
```

---

## 1. Threat Model & Enterprise Compliance

### 1.1 The "Cloud Web Formatter" Vulnerability
Conventional online developer utilities rely on backend server roundtrips:
1. The developer pastes a JWT or JSON payload into a textarea.
2. The browser sends an HTTP `POST /api/format` or `POST /api/decode`.
3. The remote web server parses the payload. In doing so, the payload is frequently recorded in:
   - Web application reverse proxy access logs (Nginx, Cloudflare, AWS ALB).
   - Application Performance Monitoring (APM) traces (Datadog, Sentry, New Relic).
   - Ingress WAF caches and inspection pipelines.
4. If an engineer pastes an active production JWT or an unredacted database export, credentials and PII immediately escape corporate security perimeters.

### 1.2 The Air-Gapped Client-Side Invariant
Toolbox eliminates this attack surface entirely by enforcing an invariant:

$$\text{Payload Transmission} = \emptyset$$

No user-supplied payload, file, image, token, or string is ever transmitted across the network. All operations run client-side inside the user's browser V8 or JavaScriptCore runtime.

---

## 2. Technical Implementation Pillars

### 2.1 W3C Web Cryptography API (`crypto.subtle`)
All cryptographic primitives—including SHA-256/SHA-512 hashing, HMAC authentication, AES-GCM 256-bit encryption, and RSA/ECC keypair generation—rely on the standard browser [W3C Web Cryptography API](https://www.w3.org/TR/WebCryptoAPI/).
- Keys and IVs (Initialization Vectors) are derived using `window.crypto.getRandomValues()`, which sources cryptographically secure entropy directly from the underlying operating system kernel (`/dev/urandom` or Windows CNG).
- Cryptographic keys remain isolated in browser memory as non-extractable `CryptoKey` handles whenever applicable.

### 2.2 Client-Side AST Parsing & Tokenization
- **JSON Formatting & AST Healing**: Parsed using native `JSON.parse` and in-memory Abstract Syntax Tree (AST) parsers running inside the main thread or dedicated Web Workers.
- **cURL Translation**: Translated directly into fetch/Python/Go ASTs using lexical scanner state machines executing purely in client JavaScript.
- **RegEx Evaluation**: Executed against the client's native JavaScript regex engine with built-in catastrophic backtracking heuristics to prevent ReDoS from locking the browser tab.

### 2.3 HTML5 Canvas & WebAssembly Media Processing
- **Image Compression & Format Conversion**: Images selected by the user are loaded via the File API (`FileReader.readAsDataURL` or `createObjectURL`) into an HTML5 `<canvas>` element. Resizing, quantization, and quality compression operate through local canvas rendering contexts without server roundtrips.
- **EXIF Stripping**: Binary file headers (TIFF/JPEG markers) are sliced and reconstructed directly using `ArrayBuffer` and `DataView` operations in RAM.

---

## 3. Network Hardening & Content Security Policy (CSP)

To guarantee that code running on Toolbox cannot inadvertently leak data, the platform deploys strict HTTP response headers:

```http
Content-Security-Policy: default-src 'self'; script-src 'self' 'unsafe-eval' 'unsafe-inline' https://pagead2.googlesyndication.com https://fundingchoicesmessages.google.com https://www.googletagmanager.com https://static.cloudflareinsights.com; style-src 'self' 'unsafe-inline'; img-src 'self' blob: data: https://flagcdn.com https://pagead2.googlesyndication.com; font-src 'self' data:; connect-src 'self' https://pagead2.googlesyndication.com https://fundingchoicesmessages.google.com https://www.google-analytics.com https://www.googletagmanager.com https://cloudflareinsights.com; frame-src 'self' https://googleads.g.doubleclick.net https://fundingchoicesmessages.google.com; worker-src 'self' blob:; object-src 'none'; base-uri 'self'; form-action 'self';
X-Content-Type-Options: nosniff
Referrer-Policy: strict-origin-when-cross-origin
Strict-Transport-Security: max-age=63072000; includeSubDomains; preload
Permissions-Policy: camera=(), microphone=(), geolocation=()
```

### Key Security Safeguards:
1. **`form-action 'self'`**: Form submissions cannot post user data to external endpoints.
2. **`object-src 'none'`**: Disables Flash, Java applets, and legacy plugin vectors.
3. **`Permissions-Policy`**: Disables access to sensitive hardware (webcam, microphone, GPS).
4. **Isolated Web Workers**: Heavy processing (such as large JSON repair or multi-file image compression) runs in ephemeral Blob workers isolated from the DOM.

---

## 4. Ephemeral Memory Lifecycle

1. **Zero Persistence of Sensitive Data**: Toolbox does not store input payloads in `localStorage`, `sessionStorage`, or `IndexedDB`.
2. **Garbage Collection**: Once an operation completes and the input textarea is cleared or the browser tab is closed, all allocated string buffers and AST nodes are immediately eligible for V8 garbage collection (`Mark-Sweep-Compact`).
3. **No Service Worker Caching of Payloads**: Service worker caches are strictly configured to store immutable static assets (JavaScript, CSS, fonts, icons) and never cache dynamic user input or query strings.

---

## 5. Verification & Auditing

You can verify the client-side guarantee yourself in under 30 seconds:
1. Open Chrome DevTools (`Cmd + Option + I` or `Ctrl + Shift + I`).
2. Switch to the **Network** tab and check **Preserve log**.
3. Filter by **Fetch/XHR**.
4. Paste any sensitive test string into the [JWT Decoder](https://toolbox.vishnudigital.com/jwt-decoder), [JSON Formatter](https://toolbox.vishnudigital.com/json-formatter), or [cURL Converter](https://toolbox.vishnudigital.com/curl).
5. **Observation**: Notice that exactly **zero** network requests are dispatched as the tool decodes, formats, and transforms your input in real-time.

---

## Contact & Security Disclosures

For security assessments, enterprise audits, or coordinated vulnerability disclosures:
- **Email**: `contact@toolbox.vishnudigital.com`
- **Security Policy**: [SECURITY.md](../../SECURITY.md)
- **Official Website**: [https://toolbox.vishnudigital.com](https://toolbox.vishnudigital.com)
