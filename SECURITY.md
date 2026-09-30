# Security Policy

## Supported Versions

Toolbox is a client-side web platform running directly in browser memory at [https://toolbox.vishnudigital.com](https://toolbox.vishnudigital.com). All users access the latest deployed version automatically.

| Version / Deployment | Supported          |
| -------------------- | ------------------ |
| Web Production       | :white_check_mark: |
| Self-hosted / Forks  | :x:                |

## Reporting a Vulnerability

The Toolbox engineering team takes the security and privacy of our client-side architecture seriously. Because all processing occurs exclusively in browser RAM with zero server telemetry, security concerns typically relate to:
- Client-side cryptographic implementation flaws (WebCrypto usage, entropy, padding).
- Unintended external network requests or third-party leakage.
- Cross-Site Scripting (XSS) vectors in AST parsing, formatters, or HTML/SVG preview renderers.

### Disclosure Process

1. **Do NOT open a public GitHub issue** for undisclosed security vulnerabilities.
2. Email the security team directly at **`contact@toolbox.vishnudigital.com`** with:
   - Tool slug or URL where the issue was observed.
   - Detailed step-by-step reproduction instructions or a minimal proof-of-concept (PoC).
   - Impact assessment (e.g., memory leakage, DOM XSS, crypto weakness).
3. You will receive an acknowledgment within **48 hours**.
4. We coordinate patch deployment directly to production and credit researchers in the release notes upon verification.
