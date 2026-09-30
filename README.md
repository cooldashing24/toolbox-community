<div align="center">

# 🧰 Toolbox — Public Directory & Community Hub
### Global, Air-Gapped, Zero-Telemetry Developer Utilities Running 100% in Browser Memory

[![Web App](https://img.shields.io/badge/Web%20App-Live-success?style=flat-square&logo=google-chrome)](https://toolbox.vishnudigital.com)
[![Engineering Blog](https://img.shields.io/badge/Guides-Toolbox%20Blog-blue?style=flat-square)](https://blog.toolbox.vishnudigital.com)
[![Zero Telemetry](https://img.shields.io/badge/Privacy-100%25%20Client--Side%20RAM-success?style=flat-square)](https://toolbox.vishnudigital.com/privacy)
[![WebCrypto API](https://img.shields.io/badge/WebCrypto-W3C%20Standard-blueviolet?style=flat-square)](https://www.w3.org/TR/WebCryptoAPI/)

**[Explore Live Tools](https://toolbox.vishnudigital.com) • [Engineering Guides](https://blog.toolbox.vishnudigital.com) • [Request a Tool](https://github.com/toolbox/toolbox-community/issues/new/choose) • [Report a Bug](https://github.com/toolbox/toolbox-community/issues/new/choose)**

</div>

---

## ⚡ What is Toolbox?

**[Toolbox](https://toolbox.vishnudigital.com)** is a global, proprietary, air-gapped web platform providing **42+ high-performance developer utilities** accessible worldwide to software engineers, systems architects, and security teams.

### The Enterprise Compliance Dilemma
Under **SOC2, HIPAA, GDPR, and ISO 27001**, corporate security policies strictly forbid engineers from pasting customer session tokens, proprietary database schemas, private keys, or API payloads into public web formatters that log requests to cloud servers.

**Toolbox was engineered specifically to solve this problem globally:**
* 🌍 **Global Web Availability**: Delivered instantly across global edge networks with zero desktop software to install, zero dependencies, and instant web access.
* 🔒 **100% Client-Side In-Browser Execution**: All cryptographic algorithms, regex matchers, AST parsers, and conversions execute exclusively inside your browser memory via WebCrypto, client-side ASTs, and HTML5 Canvas.
* 🚫 **Zero Server Telemetry**: No tokens, credentials, schemas, or files are ever transmitted to any remote backend server.
* ✈️ **Offline & Air-Gapped Capable**: Works seamlessly in restricted enterprise environments with zero outbound network calls once loaded.

---

## 🛠️ Flagship Tools & Verified Technical Guides

| Tool Category | Live Interactive Workbench | Authoritative Technical Guide | Use Cases & Production Scenarios |
| :--- | :--- | :--- | :--- |
| **Auth & Security** | [JWT Token Inspector](https://toolbox.vishnudigital.com/jwt-decoder) | [JWT Claims & Security Guide](https://blog.toolbox.vishnudigital.com/jwt-security-101-decode-inspect-claims-guide/) | • 2 AM auth outage triages without cloud secret leaks.<br>• Auditing OIDC `iss` & `aud` claims before deploying route guards.<br>• Investigating `RS256` to `HS256` Key Confusion vulnerabilities. |
| **Regex & Parsing** | [RegEx Tester & Group Matcher](https://toolbox.vishnudigital.com/regex-tester) | [ReDoS Prevention Guide](https://blog.toolbox.vishnudigital.com/regex-backtracking-redos-prevention-guide/) | • Pre-deploy audits detecting $2^{n-1}$ catastrophic backtracking loops.<br>• Character offset span & named capture group visualization.<br>• Testing patterns against confidential customer logs safely in browser RAM. |
| **API Translation** | [cURL to Code Converter](https://toolbox.vishnudigital.com/curl) | [cURL Automated Translation Guide](https://blog.toolbox.vishnudigital.com/curl-to-code-converter-guide/) | • Converting Chrome DevTools "Copy as cURL" into Go/Python/Rust client code.<br>• Translating complex Bearer tokens without leaking secrets to 3rd-party loggers.<br>• Eliminating Windows PowerShell quote escaping errors. |
| **AI & LLM Ops** | [LLM JSON Output Healer](https://toolbox.vishnudigital.com/json-repair) | [LLM JSON Repair & Truncation Guide](https://blog.toolbox.vishnudigital.com/llm-json-repair-guide/) | • Rescuing truncated JSON arrays severed by model `max_tokens` ceilings.<br>• Stripping DeepSeek `<think>` reasoning preambles before DB insertion.<br>• Normalizing LangChain Python dict dumps (`None`/`True`/`False`). |
| **Type Safety** | [JSON Schema to TypeScript & Zod](https://toolbox.vishnudigital.com/json-schema-to-typescript) | [Type Safety & Contract Drift Guide](https://blog.toolbox.vishnudigital.com/json-schema-to-typescript-zod-guide/) | • Protecting API ingestion boundaries with runtime Zod validation.<br>• Eliminating contract drift between backend schemas and frontend types.<br>• Generating type-checked Stripe and Shopify webhook event handlers. |
| **Data Pipelines** | [HTML to Markdown AST Studio](https://toolbox.vishnudigital.com/html-to-markdown) | [HTML to Markdown AST Pipeline Guide](https://blog.toolbox.vishnudigital.com/html-to-markdown-ast-pipeline-guide/) | • Stripping 60–78% non-semantic HTML boilerplate from web scrapes for RAG.<br>• Converting messy Google Docs or Confluence tables into GFM.<br>• Processing internal confidential documentation with zero server uploads. |

---

## 🌐 Complete Directory of 42+ Live Utilities

### 🔐 Cryptography, Privacy & Security
* [Hash & HMAC Generator](https://toolbox.vishnudigital.com/hash-generator) — Compute SHA-256, SHA-512, MD5, and HMAC signatures in browser memory.
* [TOTP Authenticator & Code Generator](https://toolbox.vishnudigital.com/totp-authenticator) — Live RFC 6238 2FA codes with 30-second countdowns.
* [AES-GCM Encryption / Decryption](https://toolbox.vishnudigital.com/aes-encryption) — Authenticated symmetric encryption using W3C WebCrypto.
* [RSA & ECC Keypair Studio](https://toolbox.vishnudigital.com/rsa-keys) — Generate PEM-encoded cryptographic key pairs in browser memory.
* [SSL / X.509 Certificate Inspector](https://toolbox.vishnudigital.com/ssl-cert-parser) — Inspect SANs, intermediate chains, and validity periods without server uploads.

### 💻 Developer Tools & Formatters
* [JSON Formatter & Validator](https://toolbox.vishnudigital.com/json-formatter) — High-speed AST JSON formatting, syntax validation, and minification.
* [Base64 & Data URI Studio](https://toolbox.vishnudigital.com/base64-studio) — RFC 4648 encoding and RFC 2397 Data URI generation for images and text.
* [UUID v4 vs v7 Generator](https://toolbox.vishnudigital.com/uuid-generator) — Generate cryptographically secure random v4 and time-ordered v7 UUIDs.
* [IPv4 Subnet & CIDR Calculator](https://toolbox.vishnudigital.com/subnet-calculator) — Calculate network boundaries, broadcast addresses, and assignable host ranges.
* [Cron Expression Builder](https://toolbox.vishnudigital.com/cron-generator) — Visual 5-field crontab builder with human-readable schedule explanations.
* [URL Percent Encoder / Decoder](https://toolbox.vishnudigital.com/url-encode) — Strict RFC 3986 percent-encoding for query parameters.
* [SQL Query Explainer](https://toolbox.vishnudigital.com/sql-explainer) — Visual query plan breakdown and indexing advice.

### 📝 Text, Media & Document Processing
* [Word & Character Counter](https://toolbox.vishnudigital.com/word-count) — Real-time reading time, word metrics, and frequency distribution.
* [String Case Converter](https://toolbox.vishnudigital.com/case-converter) — Convert between camelCase, snake_case, kebab-case, and PascalCase.
* [Markdown Table Generator](https://toolbox.vishnudigital.com/markdown-table-generator) — Visual grid editor exporting clean GFM tables.
* [EXIF & Photo Metadata Stripper](https://toolbox.vishnudigital.com/exif-viewer) — Losslessly strip GPS coordinates and camera serials in client RAM.
* [PDF Merger & Splitter](https://toolbox.vishnudigital.com/pdf-merge) — Combine or split PDF documents in browser without uploading files to remote servers.
* [Image Size Compressor](https://toolbox.vishnudigital.com/compress-image-to-size) — Compress JPEG/PNG/WebP assets to exact byte limits (100KB, 200KB, 500KB) in browser canvas.

---

## 📚 Architectural & Downstream Recipes

* [100% Client-Side Privacy Architecture](docs/privacy-architecture.md) — Technical breakdown of WebCrypto sandboxing, CSP policies, and zero server telemetry.
* [Zod Webhook Validation Recipe](docs/recipes/zod-webhook-validation.md) — Protect ingestion boundaries and eliminate schema contract drift.
* [Safe Client-Side JWT Handling Recipe](docs/recipes/safe-jwt-client-handling.md) — Inspect token expiration and claims safely without third-party bloat.
* [cURL to Fetch Integration Recipe](docs/recipes/curl-to-fetch-integration.md) — Transform Chrome DevTools cURL captures into production-grade TypeScript API wrappers.

---

## 💡 Community & Support

* **Feature Requests**: Have a developer utility you'd love to see in Toolbox? [Submit a Tool Request](https://github.com/toolbox/toolbox-community/issues/new?template=feature_request.yml).
* **Bug Reports**: Found an edge case with one of our client-side tools? [Open an Issue](https://github.com/toolbox/toolbox-community/issues/new?template=bug_report.yml).
* **Security & Vulnerability Disclosure**: Please review our [Security Policy](SECURITY.md) to report vulnerabilities privately.

---

## ⚖️ License & Terms

* Documentation and public integration guides are licensed under [CC-BY-4.0](LICENSE).
* Community integration recipes under `docs/recipes/` are licensed under [MIT](LICENSE).
* The **Toolbox** and **Toolbox Blog** web applications are proprietary, closed-source services maintained by the **[Toolbox Engineering Team](https://toolbox.vishnudigital.com)**.
