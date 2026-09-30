<div align="center">

# 🧰 Toolbox — Public Directory & Community Hub
### Global, Air-Gapped, Zero-Telemetry Developer Utilities (200+ Tools) Running 100% in Browser Memory

[![Web App](https://img.shields.io/badge/Web%20App-Live-success?style=flat-square&logo=google-chrome)](https://toolbox.vishnudigital.com)
[![Engineering Blog](https://img.shields.io/badge/Guides-Toolbox%20Blog-blue?style=flat-square)](https://blog.toolbox.vishnudigital.com)
[![Zero Telemetry](https://img.shields.io/badge/Privacy-100%25%20Client--Side%20RAM-success?style=flat-square)](https://toolbox.vishnudigital.com/privacy)
[![WebCrypto API](https://img.shields.io/badge/WebCrypto-W3C%20Standard-blueviolet?style=flat-square)](https://www.w3.org/TR/WebCryptoAPI/)

**[Explore Live Tools](https://toolbox.vishnudigital.com) • [Engineering Guides](https://blog.toolbox.vishnudigital.com) • [Request a Tool](https://github.com/cooldashing24/toolbox-community/issues/new/choose) • [Report a Bug](https://github.com/cooldashing24/toolbox-community/issues/new/choose)**

</div>

---

## ⚡ What is Toolbox?

**[Toolbox](https://toolbox.vishnudigital.com)** is a global, proprietary, air-gapped web platform providing **200+ high-performance developer utilities** accessible worldwide to software engineers, systems architects, and security teams.

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
| **Data & JSON AST** | [JSON Formatter & Validator](https://toolbox.vishnudigital.com/json-formatter) | [JSON Formatting & AST Validation Guide](https://blog.toolbox.vishnudigital.com/how-to-format-validate-json-online/) | • Formats, validates, and minifies massive JSON structures in memory.<br>• Hierarchical node navigation without uploading payload to cloud servers.<br>• Detects syntax errors, missing delimiters, and unescaped quotes instantly. |
| **Cryptography** | [Multi-Algorithm Hash Generator](https://toolbox.vishnudigital.com/hash-generator) | [Cryptographic Hash Verification Guide](https://blog.toolbox.vishnudigital.com/how-to-generate-sha256-md5-hashes-online/) | • Computes MD5, SHA-1, SHA-256, SHA-512, and HMAC signatures in browser RAM.<br>• Client-side file checksum validation against release hashes without uploads.<br>• Instant hex and Base64 digest generation. |
| **Distributed IDs** | [UUID v4 & v7 Identifier Generator](https://toolbox.vishnudigital.com/uuid-generator) | [UUID Collision & Timestamp Guide](https://blog.toolbox.vishnudigital.com/understanding-uuid-v4-vs-v7-generation-guide/) | • Generates RFC 4122 v4 random and RFC 9562 v7 time-ordered UUIDs.<br>• Database index B-Tree locality optimization with millisecond timestamp prefixes.<br>• Zero collision risk for distributed database keys and batch creation. |
| **Cloud Networking** | [Subnet Calculator Online](https://toolbox.vishnudigital.com/subnet-calculator) | [IPv4 Subnets & CIDR Blocks Guide](https://blog.toolbox.vishnudigital.com/how-to-calculate-ipv4-subnets-cidr-blocks-guide/) | • Calculates IPv4 & IPv6 subnet boundaries, CIDR prefixes, and wildcard masks.<br>• Visual 32-bit bitmask matrix and usable host range calculations.<br>• Cloud VPC architecture planning (AWS, GCP, Azure). |
| **Data Pipelines** | [HTML to Markdown AST Studio](https://toolbox.vishnudigital.com/html-to-markdown) | [HTML to Markdown AST Pipeline Guide](https://blog.toolbox.vishnudigital.com/html-to-markdown-ast-pipeline-guide/) | • Stripping 60–78% non-semantic HTML boilerplate from web scrapes for RAG.<br>• Converting messy Google Docs or Confluence tables into GFM.<br>• Processing internal confidential documentation with zero server uploads. |

---

## 🌐 Complete Directory of 200+ Live Utilities

### 🔐 Security & Cryptography
* [AES-GCM & AES-CBC Encryption](https://toolbox.vishnudigital.com/aes-encryption) — Encrypt and decrypt text messages with AES-GCM and AES-CBC using client-side Web Crypto API.
* [RSA Keypair Generator](https://toolbox.vishnudigital.com/rsa-keys) — Generate 2048/4096-bit RSA public and private keypairs in standard PEM PKCS#8 format.
* [HMAC Signature Generator & Verifier](https://toolbox.vishnudigital.com/hmac-generator) — Generate and verify HMAC-SHA256, HMAC-SHA512, and HMAC-SHA1 signatures with secret keys.
* [TOTP 2FA Authenticator Simulator](https://toolbox.vishnudigital.com/totp-authenticator) — Generate and test RFC 6238 Time-based One-Time Passwords (TOTP) from base32 secret seeds.
* [BIP39 Mnemonic Seed Generator](https://toolbox.vishnudigital.com/bip39-generator) — Generate cryptographically secure 12 and 24-word BIP39 crypto wallet mnemonic seed phrases.
* [Random Secure Password Generator](https://toolbox.vishnudigital.com/password-generator) — Generate cryptographically secure random passwords with configurable character sets and entropy scoring.
* [Password Strength & Entropy Checker](https://toolbox.vishnudigital.com/password-strength) — Analyze password entropy bits, brute-force crack time estimates, and pattern vulnerabilities.
* [Caesar Cipher Encoder & Decoder](https://toolbox.vishnudigital.com/caesar-cipher) — Encrypt and decrypt classic Caesar substitution ciphers with custom shift values.
* [Vigenère Polyalphabetic Cipher](https://toolbox.vishnudigital.com/vigenere-cipher) — Encrypt and decrypt text using polyalphabetic Vigenère tabula recta substitution.
* [Morse Code Audio & Text Translator](https://toolbox.vishnudigital.com/morse-code-translator) — Translate text to Morse code and decode Morse with Web Audio tone playback.
* [Private Legal & Document PDF Redactor](https://toolbox.vishnudigital.com/pdf-redactor) — Apply forensic diagonal watermarks, sequential Bates numbering, and permanent blackout redactions to PDFs 100% locally.
* [Multi-Algorithm Hash & HMAC Generator](https://toolbox.vishnudigital.com/hash-generator) — Compute MD5, SHA-1, SHA-256, SHA-512, SHA-3, and HMAC signatures in browser with file checksum matching.
* [JWT Inspector & Signature Verifier](https://toolbox.vishnudigital.com/jwt-debugger) — Decode JSON Web Tokens, inspect claims, calculate expiration countdowns, and verify signatures in browser RAM.
* [RSA & ECC Key Pair Generator](https://toolbox.vishnudigital.com/key-generator) — Generate cryptographically secure RSA and ECC public and private key pairs with PEM and JWK exports.
* [SSL/TLS Certificate & ASN.1 X.509 Parser](https://toolbox.vishnudigital.com/ssl-cert-parser) — Parse PEM and ASN.1 DER X.509 certificates, verify SAN domains, and calculate SHA-256 fingerprints.

### 💻 Developer & Data Tools
* [Algorithm Visualizer & Multi-Race](https://toolbox.vishnudigital.com/algorithm-visualizer) — Interactive real-time visualization of sorting, pathfinding (A*, Dijkstra), and tree traversals.
* [In-Browser SQL Studio & SQLite WASM](https://toolbox.vishnudigital.com/sql-studio) — Execute SQL queries, load schemas, import CSVs, and analyze execution plans client-side via SQLite WASM.
* [CSV to SQL Schema & Batch Converter](https://toolbox.vishnudigital.com/csv-to-sql) — Convert CSV data to SQL CREATE TABLE schema and batched INSERT statements with automatic type inference across PostgreSQL, MySQL, SQLite, MSSQL, and Oracle.
* [Regex State Machine Visualizer](https://toolbox.vishnudigital.com/regex-visualizer) — Interactive AST and DFA/NFA state machine visualizer for regular expressions.
* [Java Execution Visualizer](https://toolbox.vishnudigital.com/java-visualizer) — Step-by-step Java code visualizer tracking stack frames, heap objects, and variable states.
* [JSON Formatter & Validator](https://toolbox.vishnudigital.com/json-formatter) — Format, validate, minify, and inspect JSON with hierarchical tree navigation and syntax highlighting.
* [JWT Token Inspector & Decoder](https://toolbox.vishnudigital.com/jwt-decoder) — Decode and inspect RFC 7519 JSON Web Tokens, headers, payload claims, and expiration timestamps.
* [JSON to TypeScript Interface Converter](https://toolbox.vishnudigital.com/json-to-typescript) — Convert raw JSON payloads into strongly typed TypeScript interfaces and type definitions.
* [JSON Schema to TypeScript & Zod](https://toolbox.vishnudigital.com/json-schema-to-typescript) — Compile draft-07/2020-12 JSON Schemas into TypeScript types and Zod validation schemas.
* [JSON to TOON LLM Prompt Compressor](https://toolbox.vishnudigital.com/json-to-toon) — Compress structured JSON data into token-efficient TOON format for LLM prompts.
* [cURL to Multi-Language Code Converter](https://toolbox.vishnudigital.com/curl) — Convert cURL commands to Fetch, Axios, Python Requests, Go, Rust, and Swift code snippets.
* [SQL Formatter & Beautifier](https://toolbox.vishnudigital.com/sql-format) — Format, beautify, and indent messy SQL queries with dialect-specific keyword casing.
* [HAR Waterfall Analyzer](https://toolbox.vishnudigital.com/har-analyzer) — Inspect browser HTTP Archive (HAR) files, analyze TTFB latency, and find network bottlenecks.
* [SSL / X.509 Certificate Inspector](https://toolbox.vishnudigital.com/cert-inspector) — Decode PEM/DER SSL certificates client-side. Inspect SAN domains, expiry dates, and trust chains.
* [LLM Token Budget & Cost Matrix](https://toolbox.vishnudigital.com/llm-tokens) — Count tokens across BPE tokenizers and compare pricing across frontier AI models.
* [LLM JSON Healer & Repair](https://toolbox.vishnudigital.com/llm-json-repair) — Automatically repair truncated AI JSON, fix missing brackets, unescaped quotes, and strip reasoning tags.
* [Air-Gapped Prompt DLP Redactor](https://toolbox.vishnudigital.com/prompt-redactor) — Scrub API keys, credit cards, emails, IP addresses, and PII from prompts before sending to AI models.
* [Webhook Signature Simulator](https://toolbox.vishnudigital.com/webhook-tester) — Simulate and verify HMAC webhook signatures for Stripe, GitHub, Shopify, and Razorpay.
* [Unix Chmod Permissions Calculator](https://toolbox.vishnudigital.com/chmod-calculator) — Calculate octal (e.g. 755), symbolic (rwxr-xr-x), and umask permissions for Unix file systems.
* [SVG Optimizer & Minifier](https://toolbox.vishnudigital.com/svg-optimizer) — Minify vector SVGs, strip metadata, optimize paths, and export JSX React components.
* [Color Palette & WCAG Studio](https://toolbox.vishnudigital.com/color-palette) — Generate color palettes, Tailwind CSS scales, and test WCAG 2.2 contrast compliance.
* [SQL & JSON Mock Data Synthesizer](https://toolbox.vishnudigital.com/mock-data) — Generate synthetic test datasets in SQL INSERT, JSON, CSV, and TypeScript formats.
* [Base64 Image Converter](https://toolbox.vishnudigital.com/base64-image) — Convert PNG, JPG, and WebP images to Base64 Data URIs and decode strings back to images.
* [Base64 Encoder & Decoder](https://toolbox.vishnudigital.com/base64-converter) — Encode text and binary strings to RFC 4648 standard Base64 and decode back instantly.
* [URL Percent Encoder & Decoder](https://toolbox.vishnudigital.com/url-encode) — Percent-encode special characters in URLs and query strings per RFC 3986.
* [RegEx Tester & Group Matcher](https://toolbox.vishnudigital.com/regex-tester) — Test regular expressions in real-time with syntax highlighting and capture group inspection.
* [UUID v4 & v7 Identifier Generator](https://toolbox.vishnudigital.com/uuid-generator) — Generate cryptographically secure RFC 4122 Version 4 and time-ordered Version 7 UUIDs.
* [URL Slug Generator](https://toolbox.vishnudigital.com/slug-generator) — Transform strings into SEO-friendly, clean, hyphenated URL slugs.
* [Text & Code Diff Checker](https://toolbox.vishnudigital.com/diff-checker) — Compare two text snippets with side-by-side or inline character/line diffs.
* [Number Base Converter](https://toolbox.vishnudigital.com/base-convert) — Convert numbers between Binary, Octal, Decimal, and Hexadecimal notations.
* [Color Format Converter](https://toolbox.vishnudigital.com/color-converter) — Convert colors between HEX, RGB, HSL, and CMYK formats with live canvas preview.
* [Docker Run to Compose Converter](https://toolbox.vishnudigital.com/docker-converter) — Convert single docker run CLI commands into clean compose.yaml Docker Compose files.
* [Environment (.env) Converter](https://toolbox.vishnudigital.com/env-converter) — Convert .env variables to Kubernetes ConfigMap, Secret, JSON, Docker Compose YAML, Shell scripts, and Terraform tfvars.
* [HTML Entities Encoder & Decoder](https://toolbox.vishnudigital.com/html-entities) — Convert special characters into HTML named entities and decode numeric codes.
* [JavaScript Keycode Event Inspector](https://toolbox.vishnudigital.com/javascript-keycode-finder) — Inspect live keyboard event properties (event.key, event.code, keyCode, modifiers).
* [User-Agent & Device Inspector](https://toolbox.vishnudigital.com/user-agent) — Parse browser User-Agent strings, operating system, rendering engine, and device screen metrics.
* [Cron Expression Builder & Explainer](https://toolbox.vishnudigital.com/cron-generator) — Build and translate standard 5-part cron expressions into human-readable schedules.
* [CSV to JSON & JSON to CSV Converter](https://toolbox.vishnudigital.com/csv-json-converter) — Convert tabular CSV files to JSON objects and convert JSON arrays to CSV downloads.
* [YAML to JSON & JSON to YAML Converter](https://toolbox.vishnudigital.com/yaml-json-converter) — Bidirectional YAML and JSON parser with syntax validation and indentation formatting.
* [Social Meta Tags & SERP Previewer](https://toolbox.vishnudigital.com/social-preview) — Live visual previewer for Google Search, X (Twitter), LinkedIn, and Discord with HTML & Next.js metadata generation.
* [Social Banner & OpenGraph Automation Engine](https://toolbox.vishnudigital.com/social-banner-engine) — Design 1200x630 OpenGraph cards, batch-convert markdown frontmatter, and generate zero-dependency CI/CD build scripts.
* [PDF Text Extractor – Extract Text from PDF Online](https://toolbox.vishnudigital.com/pdf-text-extractor) — Extract the embedded text layer from a PDF document directly in your browser and copy or download it as plain text, with 100% client-side privacy.
* [Code Minifier Online](https://toolbox.vishnudigital.com/code-minifier) — Compress JavaScript, HTML, CSS, JSON, SQL, and GraphQL code with instant byte-savings calculations.
* [Code Beautifier & Formatter](https://toolbox.vishnudigital.com/code-beautifier) — Prettify, indent, and format JS/TS, HTML, CSS, JSON, SQL, and GraphQL code with custom indentation rules.
* [Base64 Data URL Studio](https://toolbox.vishnudigital.com/base64-studio) — Encode files, images, SVG, and audio into RFC 2397 Data URIs with live canvas previews and HTML/CSS snippets.
* [Hex Dump Online](https://toolbox.vishnudigital.com/hex-dump) — Inspect binary byte streams with canonical 16-byte offset rows, ASCII gutter, Endianness toggle, and C array exports.
* [Bitmask Calculator Online](https://toolbox.vishnudigital.com/bitmask-calculator) — Interactive 8/16/32/64-bit clickable bit matrices with multi-radix synchronization and bitwise ALU operations.
* [JSON to Types Generator](https://toolbox.vishnudigital.com/json-to-types) — Generate strongly typed TypeScript, Zod, Python, Rust, and Go types from arbitrary JSON payloads.
* [JSON Schema Generator](https://toolbox.vishnudigital.com/json-schema-generator) — Infer Draft-07 and Draft 2020-12 JSON Schemas with semantic format detection (email, date, uri, uuid).
* [In-Browser Mock API Studio](https://toolbox.vishnudigital.com/mock-api-studio) — Simulate custom REST API routes, HTTP status codes, latency delays, and export cURL/Fetch snippets.
* [DNS Lookup Online (DoH)](https://toolbox.vishnudigital.com/dns-lookup) — Query DNS records (A, AAAA, CNAME, MX, TXT, NS, SOA, CAA) over DNS-over-HTTPS with zero server logging.
* [Subnet Calculator Online](https://toolbox.vishnudigital.com/subnet-calculator) — Calculate IPv4 & IPv6 subnet boundaries, CIDR prefixes, wildcard masks, and 32-bit bitmask matrix.
* [HTTP Header Security Auditor](https://toolbox.vishnudigital.com/http-headers) — Inspect HTTP response headers, audit OWASP security compliance, and generate server hardening rules.
* [CSS Grid & Flexbox Interactive Studio](https://toolbox.vishnudigital.com/css-layout-studio) — Design responsive CSS Grid and Flexbox layouts visually and export clean Tailwind CSS 4 and pure CSS code.
* [Cubic Bezier & Spring Motion Studio](https://toolbox.vishnudigital.com/spring-curve-generator) — Simulate damped harmonic spring physics, manipulate cubic-bezier curves, and export CSS linear() easing.
* [Glassmorphism & Mesh Gradient Generator](https://toolbox.vishnudigital.com/glass-mesh-generator) — Design radial mesh gradients and frosted glass backdrop filters with Tailwind CSS 4 and pure CSS export.
* [Protobuf Schema & Binary Decoder](https://toolbox.vishnudigital.com/protobuf-decoder) — Decode Google Protocol Buffers binary wire format and map fields with optional .proto schemas.
* [Apache Parquet & Arrow Data Viewer](https://toolbox.vishnudigital.com/parquet-viewer) — Inspect Apache Parquet and Arrow binary files in browser RAM, browse schema metadata, and export to CSV/JSON.
* [SQL Execution Plan & AST Visualizer](https://toolbox.vishnudigital.com/sql-explainer) — Visualize PostgreSQL & MySQL EXPLAIN ANALYZE trees, detect sequential scan bottlenecks, and get index suggestions.
* [WebSocket & SSE Live Stream Inspector](https://toolbox.vishnudigital.com/websocket-tester) — Connect to real-time WebSockets and Server-Sent Events, inspect traffic frames, and test heartbeat pings.
* [XPath & CSS Selector Live Evaluator](https://toolbox.vishnudigital.com/xpath-tester) — Test and debug XPath 3.1 expressions and CSS Selectors against HTML with live node highlighting.
* [HTML Table to JSON & CSV Scraper](https://toolbox.vishnudigital.com/html-table-scraper) — Extract, clean, and convert raw HTML tables into structured JSON, CSV, and Markdown datasets.
* [Web Metadata & Open Graph Extractor](https://toolbox.vishnudigital.com/web-metadata-extractor) — Extract Open Graph, Twitter Cards, and Schema.org JSON-LD from HTML with live social previews.

### ⏰ Time & Date Utilities
* [World Clock Grid](https://toolbox.vishnudigital.com/) — Live real-time clocks for major global financial hubs and cities worldwide.
* [Time Zone Converter](https://toolbox.vishnudigital.com/timezone-converter) — Convert and compare times across global time zones with drag-and-drop timeline sliders.
* [International Meeting Planner](https://toolbox.vishnudigital.com/meeting-planner) — Find optimal overlapping working hours across distributed global remote teams.
* [Interactive World Calendar](https://toolbox.vishnudigital.com/calendar) — National holidays, observances, and moon phases for 100+ countries.
* [Sun & Moon Astronomy Calculator](https://toolbox.vishnudigital.com/astronomy) — Calculate sunrise, sunset, golden hour, twilight, and moon phases for any coordinates.
* [Moon Phases & Lunar Calendar](https://toolbox.vishnudigital.com/moon-phases) — Track lunar illumination percentage, next full moon, and new moon dates.
* [Event Countdown Timer](https://toolbox.vishnudigital.com/countdown) — Create precision countdown timers with audio alarms and shareable live links.
* [Precision Lap Stopwatch](https://toolbox.vishnudigital.com/stopwatch) — Millisecond-accurate online stopwatch with split lap tracking and CSV export.
* [Business Days Calculator](https://toolbox.vishnudigital.com/business-days) — Calculate working days between dates excluding weekends and regional public holidays.
* [Business Hours Scheduler](https://toolbox.vishnudigital.com/business-hours) — Plan business operations and support coverage across global working hours.
* [12-Hour to 24-Hour Time Converter](https://toolbox.vishnudigital.com/time-format) — Convert between 12-hour AM/PM and 24-hour military time formats instantly.
* [Seconds to Hours & Days Converter](https://toolbox.vishnudigital.com/seconds-converter) — Convert raw seconds into days, hours, minutes, and human-readable duration strings.
* [Unix Epoch Time Explorer](https://toolbox.vishnudigital.com/unix-timestamp-converter) — Explore Unix timestamps, Year 2038 problem stats, and batch epoch conversions.
* [Discord Timestamp Generator](https://toolbox.vishnudigital.com/discord-timestamps) — Generate dynamic Discord timestamp tags (<t:timestamp:R>) for chats and bots.
* [Excel Serial Date Converter](https://toolbox.vishnudigital.com/excel-date) — Convert Microsoft Excel numeric serial dates to standard calendar dates and back.
* [Date Difference Calculator](https://toolbox.vishnudigital.com/date-difference) — Calculate exact elapsed years, months, weeks, days, hours, and minutes between two dates.
* [Future & Past Date Calculator](https://toolbox.vishnudigital.com/future-past-date) — Add or subtract days, weeks, months, or years from any starting date.
* [Leap Year Checker & Calendar](https://toolbox.vishnudigital.com/leap-year) — Check if any Gregorian calendar year is a leap year with astronomical explanations.
* [ISO Week Number Calculator](https://toolbox.vishnudigital.com/week-number) — Determine the current ISO 8601 week number, day of year, and remaining weeks.
* [Public Holidays Explorer](https://toolbox.vishnudigital.com/public-holidays) — Browse official public holidays, bank holidays, and statutory observances worldwide.
* [Pomodoro Focus Timer](https://toolbox.vishnudigital.com/pomodoro) — Interval productivity timer with custom work/break intervals and session statistics.

### 📐 Unit Converters
* [Universal Unit Converters Hub](https://toolbox.vishnudigital.com/converters) — High-precision measurement converters across 10 physical dimensions.
* [Length & Distance Converter](https://toolbox.vishnudigital.com/converters/length) — Convert meters, feet, inches, miles, kilometers, centimeters, yards, and nautical miles.
* [Weight & Mass Converter](https://toolbox.vishnudigital.com/converters/weight) — Convert kilograms, pounds, ounces, grams, stones, and metric tons.
* [Temperature Converter](https://toolbox.vishnudigital.com/converters/temperature) — Convert Celsius, Fahrenheit, and Kelvin with exact affine thermal formulas.
* [Data Storage Converter](https://toolbox.vishnudigital.com/converters/data) — Convert Bytes, Kilobytes, Megabytes, Gigabytes, Terabytes, and Petabytes.
* [Speed & Velocity Converter](https://toolbox.vishnudigital.com/converters/speed) — Convert km/h, mph, meters per second, knots, and Mach.
* [Area & Land Converter](https://toolbox.vishnudigital.com/converters/area) — Convert square meters, square feet, acres, hectares, and square kilometers.
* [Volume & Liquid Converter](https://toolbox.vishnudigital.com/converters/volume) — Convert liters, milliliters, gallons, pints, cups, and fluid ounces.
* [Pressure Converter](https://toolbox.vishnudigital.com/converters/pressure) — Convert Pascals, bar, PSI, standard atmospheres, Torr, and kilopascals.
* [Energy & Work Converter](https://toolbox.vishnudigital.com/converters/energy) — Convert Joules, calories, kilocalories, watt-hours, kWh, and BTU.
* [Fuel Efficiency Converter](https://toolbox.vishnudigital.com/converters/fuel) — Convert Miles per gallon (US & UK), km/L, and Liters per 100km (L/100km).
* [Markdown to PDF Converter](https://toolbox.vishnudigital.com/markdown-to-pdf) — Convert Markdown documents to publication-ready PDF files with themes, custom headers, page numbering, and two-column layout.

### 🧮 Calculators & Financial Tools
* [Calculators Hub](https://toolbox.vishnudigital.com/calculators) — Explore financial, mathematical, date math, and health calculators running client-side.
* [Percentage Calculator](https://toolbox.vishnudigital.com/percentage-calculator) — Calculate percentage increases, decreases, discounts, markups, and proportion ratios.
* [GST Tax Calculator](https://toolbox.vishnudigital.com/gst-calculator) — Calculate GST tax addition, removal, and CGST/SGST/IGST tax breakdowns for India.
* [Loan EMI Calculator](https://toolbox.vishnudigital.com/emi-calculator) — Calculate monthly loan EMI payments, total interest payable, and yearly amortization tables.
* [SIP Wealth & Compound Calculator](https://toolbox.vishnudigital.com/sip-calculator) — Calculate Systematic Investment Plan (SIP) returns with compounding interest and inflation adjustment.
* [PPF & EPF Retirement Calculator](https://toolbox.vishnudigital.com/ppf-epf-calculator) — Project PPF maturity value and EPF retirement corpus with year-by-year compounding breakdowns for India.
* [Loan Amortization Calculator](https://toolbox.vishnudigital.com/loan-calculator) — Calculate principal, interest schedules, and prepayment payoffs for mortgages and loans.
* [Compound & Simple Interest Calculator](https://toolbox.vishnudigital.com/compound-interest-calculator) — Calculate compound and simple investment returns with annual, quarterly, and monthly compounding.
* [Live Currency Exchange Converter](https://toolbox.vishnudigital.com/currency-converter) — Convert international currencies with live exchange rates across 150+ world currencies.
* [Exact Age Calculator](https://toolbox.vishnudigital.com/age-calculator) — Calculate exact age in years, months, days, hours, and minutes with next birthday countdown.
* [BMI & Health Category Calculator](https://toolbox.vishnudigital.com/bmi-calculator) — Calculate Body Mass Index (BMI) using Metric and Imperial units with WHO weight classifications.
* [TDEE & Calorie Burn Calculator](https://toolbox.vishnudigital.com/tdee-calculator) — Calculate Total Daily Energy Expenditure (TDEE) and Basal Metabolic Rate (BMR) with activity levels.
* [Macro & Calorie Target Calculator](https://toolbox.vishnudigital.com/macro-calculator) — Calculate daily protein, carbohydrate, and fat gram targets for cutting, bulking, and maintenance.
* [Inflation & Purchasing Power Calculator](https://toolbox.vishnudigital.com/inflation-calculator) — Calculate future inflation degradation and project the future purchasing power of your money.
* [Timesheet & Work Hours Calculator](https://toolbox.vishnudigital.com/work-hours-calculator) — Calculate daily and weekly worked hours, unpaid break deductions, and gross overtime pay.
* [Tip & Bill Splitter](https://toolbox.vishnudigital.com/tip-calculator) — Calculate tip percentages, split restaurant bills per person, and generate instant payment links.
* [Freelance Rate & Quote Calculator](https://toolbox.vishnudigital.com/freelance-rate-calculator) — Calculate the hourly rate you need to charge as a freelancer based on your income goals, billable hours, expenses, and taxes, then build project quotes with a contingency buffer.
* [Random Generator](https://toolbox.vishnudigital.com/random-number-generator) — Generate cryptographically-secure random numbers, roll dice, and flip coins directly in your browser.

### 📝 Text & Content Tools
* [Word & Character Counter](https://toolbox.vishnudigital.com/word-count) — Count words, characters, sentences, paragraphs, reading time, and speaking time in real time.
* [Text Case Converter](https://toolbox.vishnudigital.com/text-case-converter) — Convert text between camelCase, snake_case, kebab-case, UPPERCASE, lowercase, and Title Case.
* [List & Line Cleaner / Sorter](https://toolbox.vishnudigital.com/list-cleaner) — Deduplicate lines, sort alphabetically, strip blank lines, trim whitespace, and add prefixes.
* [Text Readability & Sentiment Analyzer](https://toolbox.vishnudigital.com/text-analyzer) — Analyze Flesch-Kincaid reading ease, word density, average sentence length, and vocabulary richness.
* [Lorem Ipsum Generator](https://toolbox.vishnudigital.com/lorem-ipsum-generator) — Generate customizable placeholder dummy text in paragraphs, sentences, or word counts.
* [Markdown Live Editor & Previewer](https://toolbox.vishnudigital.com/markdown-editor) — Live GitHub-flavored Markdown editor with split-screen preview, HTML export, and syntax highlighting.
* [Markdown Table Generator & Converter](https://toolbox.vishnudigital.com/markdown-table-generator) — Interactive visual spreadsheet grid for building Markdown tables and converting to CSV, TSV, HTML table, JSON, and ASCII box formats.
* [HTML to Markdown Converter](https://toolbox.vishnudigital.com/html-to-markdown) — Convert HTML markup, web articles, rich text, and clipboard snippets to clean GitHub-Flavored Markdown with GFM tables and frontmatter.
* [NATO Phonetic Alphabet Encoder & Decoder](https://toolbox.vishnudigital.com/nato-phonetic-alphabet) — Translate any text or code into NATO phonetic alphabet words (Alpha, Bravo, Charlie) with audio pronunciation, Morse code, and reverse decoding.
* [Emoji & Unicode Symbol Studio](https://toolbox.vishnudigital.com/emoji-studio) — Search 3,700+ Unicode 16.0 emojis, 3D animated variants, Japanese Kaomoji, special symbols, and Gitmoji with 8-in-1 code generator and mystery trivia.

### 🎨 Media & Image Processing
* [Audio Pitch, Tempo & EQ Studio](https://toolbox.vishnudigital.com/audio-pitch) — Shift audio pitch semitones, adjust playback tempo speed, and apply 3-band parametric EQ in-browser.
* [Audio Trimmer & Waveform Cutter](https://toolbox.vishnudigital.com/audio-cutter) — Trim audio tracks, cut MP3/WAV files, set fade-ins/outs with visual waveform scrubbers client-side.
* [Video to Animated GIF Converter](https://toolbox.vishnudigital.com/video-gif) — Convert MP4/WebM videos to optimized animated GIFs with frame rate, resolution, and palette quantization.
* [PDF Merger & Page Combiner](https://toolbox.vishnudigital.com/pdf-merge) — Combine multiple PDF documents into a single organized file with drag-and-drop page reordering.
* [PDF Page Splitter & Extractor](https://toolbox.vishnudigital.com/pdf-split) — Extract specific page ranges or split large PDF files into separate documents client-side.
* [PDF Page Organizer – Reorder, Rotate & Delete Pages](https://toolbox.vishnudigital.com/pdf-organizer) — Reorder, rotate, and delete pages inside a PDF document, then export a new file with optional structural compression, entirely in your browser.
* [Image Size Compressor](https://toolbox.vishnudigital.com/image-compressor) — Compress PNG, JPEG, and WebP image file sizes with configurable quality and resolution scaling.
* [Image Format Converter](https://toolbox.vishnudigital.com/image-converter) — Convert between PNG, JPG, WebP, AVIF, and SVG image formats with zero server upload.
* [Favicon Package Generator](https://toolbox.vishnudigital.com/favicon-generator) — Generate complete multi-size favicon suites (16x16, 32x32, 180x180, manifest) from any image.
* [EXIF & Image Metadata Stripper](https://toolbox.vishnudigital.com/exif-viewer) — Inspect and strip GPS locations, camera parameters, and private EXIF metadata from photos.
* [Aspect Ratio & Responsive Clamp() Studio](https://toolbox.vishnudigital.com/aspect-ratio) — Calculate aspect ratios (16:9, 4:3, 1:1) and generate fluid CSS clamp() responsive typography scales.
* [Box Shadow & Comic Shadow Studio](https://toolbox.vishnudigital.com/shadow-generator) — Generate smooth diffuse CSS box-shadows and tactile 2D comic block shadows.
* [WCAG & APCA Color Contrast Checker](https://toolbox.vishnudigital.com/color-contrast) — Test color contrast ratios against WCAG 2.1 AA/AAA and APCA readability standards.
* [Compress Image to Exact KB](https://toolbox.vishnudigital.com/compress-image-to-size) — Dual-pass binary search compressor for exact target kilobyte thresholds.
* [Compress Image to 100KB](https://toolbox.vishnudigital.com/compress-100kb) — Compress photos and document scans to strictly under 100KB for government and exam portals.
* [Compress Image to 200KB](https://toolbox.vishnudigital.com/compress-200kb) — Compress images under 200KB for visa applications and online submission forms.
* [Compress Image to 500KB](https://toolbox.vishnudigital.com/compress-500kb) — Shrink images under 500KB for website uploads and email attachments.
* [Passport & Visa Photo Maker](https://toolbox.vishnudigital.com/passport-photo-maker) — Biometric ICAO passport photo cropper with 4x6 and A4 printable sheets.
* [Signature Whitener & Resizer](https://toolbox.vishnudigital.com/signature-resizer) — Isolate ink strokes, clean background paper, and export transparent signature PNG under 50KB.
* [Sensitive Image Censor & Redactor](https://toolbox.vishnudigital.com/censor-image) — Pixelate, blur, and blackout sensitive private data and PII in photos 100% offline.
* [Audio Loudness Normalizer](https://toolbox.vishnudigital.com/audio-normalizer) — Normalize audio to Spotify (-14 LUFS) and Apple Music standards with true peak limiter.
* [Audio Dynamics Compressor](https://toolbox.vishnudigital.com/audio-compressor) — Interactive dynamics compressor and limiter with dynamic transfer curve visualizer.
* [Studio Voice & Mic Recorder](https://toolbox.vishnudigital.com/audio-recorder) — Studio microphone recorder with 60fps real-time waveform visualizer and lossless WAV export.
* [Multi-Track Audio Merger](https://toolbox.vishnudigital.com/audio-merger) — Combine and join multiple audio tracks with equal-power trigonometric crossfades.
* [Audio Converter & Transcoder](https://toolbox.vishnudigital.com/audio-converter) — Convert MP3, WAV, OGG, and WebM audio files with custom sample rate selection.
* [Apple HEIC to JPG Converter](https://toolbox.vishnudigital.com/heic-to-jpg) — Batch convert Apple iPhone HEIC/HEIF photos to universal JPEG format 100% in-browser.
* [Apple HEIC to PNG Converter](https://toolbox.vishnudigital.com/heic-to-png) — Convert Apple HEIC photos to lossless PNG format with full alpha channel transparency.
* [OCR Image to Text Extractor](https://toolbox.vishnudigital.com/image-to-text) — Extract text from photos, documents, and screenshots with interactive bounding boxes and confidence scores.
* [In-Browser Video Trimmer](https://toolbox.vishnudigital.com/video-trimmer) — Trim and cut video start/end clips with millisecond accuracy, live loop preview, and audio mute toggle.
* [Target-Limit Video Compressor](https://toolbox.vishnudigital.com/video-compressor) — Compress videos to exact limits for WhatsApp (16MB), Discord (8MB/25MB), and Email (25MB).
* [Video to Audio Extractor](https://toolbox.vishnudigital.com/video-to-audio) — Extract background music, voice tracks, and soundtracks from MP4 and WebM videos into lossless WAV.
* [GIF Palette Compressor & Optimizer](https://toolbox.vishnudigital.com/gif-compressor) — Reduce animated GIF file size via color palette quantization, scaling, and frame decimation.

### 🚀 Productivity & Everyday Tools
* [QR Code Studio](https://toolbox.vishnudigital.com/qr-code-generator) — Create ISO/IEC 18004 compliant QR codes for URLs, Wi-Fi, vCards, text, and cryptocurrency with SVG export.
* [UPI QR Payment Studio](https://toolbox.vishnudigital.com/upi-qr) — Generate customized NPCI standard UPI payment QR codes, printable table standees, and pay links.
* [Restaurant Table QR Standees Studio](https://toolbox.vishnudigital.com/upi-qr/table-cards) — Batch-generate printable restaurant table tent cards with embedded UPI payment QR codes and Wi-Fi access.
* [QR Standee & Table Tent Print Studio](https://toolbox.vishnudigital.com/qr-standee-studio) — Generate commercial 300 DPI vector PDF payment standees, cafe table tents, and counter displays with crop marks and batch CSV printing.
* [GST Invoice QR Code Generator](https://toolbox.vishnudigital.com/upi-qr/gst-invoice) — Generate compliant B2C GST dynamic QR codes for tax invoices per Indian tax regulations.
* [Society & Apartment Maintenance QR Notice Generator](https://toolbox.vishnudigital.com/upi-qr/society-maintenance) — Batch-generate flat-wise UPI QR payment notices for housing society and apartment maintenance collection.
* [School & Tuition Fee Collection Notice Generator](https://toolbox.vishnudigital.com/upi-qr/school-fee) — Batch-generate student-wise UPI QR fee due notices for schools and tuition classes.
* [Market Stall & Mandi Vendor QR Badge Sheet Generator](https://toolbox.vishnudigital.com/upi-qr/market-stalls) — Batch-generate per-stall UPI QR badges for markets, mandis, and exhibitions, with optional per-vendor UPI ID routing.
* [Parking & Toll Payment Sticker Generator](https://toolbox.vishnudigital.com/upi-qr/parking-sticker) — Generate a fixed-fee UPI QR sticker for parking lots, gated societies, and toll booths.
* [Auto/Taxi Driver Dashboard QR Badge Generator](https://toolbox.vishnudigital.com/upi-qr/driver-badge) — Generate a dashboard-mounted UPI QR badge for auto-rickshaw, taxi, and cab drivers to accept fares.
* [Tip Jar / Creator Support QR Card Generator](https://toolbox.vishnudigital.com/upi-qr/tip-jar) — Generate a support/tip-jar UPI QR card for street performers, riders, streamers, and freelancers.
* [Wedding & Event Shagun UPI QR Card Generator](https://toolbox.vishnudigital.com/upi-qr/wedding-shagun) — Generate a festive printable UPI QR card for collecting wedding and event shagun/gift money.
* [Donation Box UPI QR Poster Generator](https://toolbox.vishnudigital.com/upi-qr/donation-box) — Generate a large-format printable UPI QR poster for temple, NGO, and charity donation boxes.
* [Group Expense Settlement QR Generator](https://toolbox.vishnudigital.com/upi-qr/split-expenses) — Split trip and group expenses among named participants with individual per-person UPI QR codes and WhatsApp share links.
* [Delivery & COD Alternative Payment Slip Generator](https://toolbox.vishnudigital.com/upi-qr/delivery-slip) — Generate a printable UPI QR payment slip per order as a cash-on-delivery alternative for couriers and sellers.
* [Gym & Coaching Class Fee Collection Notice Generator](https://toolbox.vishnudigital.com/upi-qr/class-fee) — Batch-generate per-member UPI QR fee notices for gyms, yoga studios, and coaching classes.
* [Festival & Community Chanda Collection Notice Generator](https://toolbox.vishnudigital.com/upi-qr/festival-chanda) — Batch-generate per-household UPI QR notices for festival and community fund (chanda) collection.
* [Clinic / Doctor Consultation Fee QR Generator](https://toolbox.vishnudigital.com/upi-qr/clinic-fee) — Generate a printable UPI QR consultation-fee slip for clinics and small medical practices.
* [Vehicle Service / Garage Bill QR Generator](https://toolbox.vishnudigital.com/upi-qr/garage-bill) — Generate a printable UPI QR bill slip for mechanics, garages, and vehicle service centers.
* [Print Shop / Photocopy Kiosk UPI QR Sticker Generator](https://toolbox.vishnudigital.com/upi-qr/print-shop) — Generate a kiosk-style UPI QR sticker for pay-per-job print shops, photocopy counters, and shared printers.
* [Crowdfunding / Fundraiser Campaign UPI QR Poster Generator](https://toolbox.vishnudigital.com/upi-qr/crowdfunding) — Generate a large-format printable UPI QR poster for cause-based fundraising campaigns with a stated goal.
* [Service Booking Advance / Deposit QR Generator](https://toolbox.vishnudigital.com/upi-qr/booking-deposit) — Generate a printable UPI QR slip for collecting service booking advances and deposits.
* [Vendor Advance / Security Deposit Slip Generator](https://toolbox.vishnudigital.com/upi-qr/security-deposit) — Generate a printable UPI QR slip for collecting refundable rental and equipment security deposits.
* [Recurring Flatmate Bill Splitter](https://toolbox.vishnudigital.com/upi-qr/flatmate-bills) — Split recurring monthly flatmate bills like electricity and wifi, with saved roommate groups and per-person UPI QR codes.
* [Rent Receipt with QR](https://toolbox.vishnudigital.com/upi-qr/rent-receipt) — Generate a monthly rent payment UPI QR with an auto-numbered printable receipt and local receipt history.
* [Installment Payment Plan Generator](https://toolbox.vishnudigital.com/upi-qr/installment-plan) — Split a total amount into installment QR codes with due dates, and export the schedule as a downloadable calendar file.
* [Multi-Vendor Event Budget Tracker](https://toolbox.vishnudigital.com/upi-qr/event-budget) — Track wedding and event vendor payments against a total budget, with per-vendor UPI QR codes and running balance.
* [Chit Fund / Committee (BC) Rotation Tracker](https://toolbox.vishnudigital.com/upi-qr/chit-fund) — Track a rotating savings committee's monthly contribution schedule, payout rotation, and per-member UPI QR codes.
* [Freelance Milestone Payment Tracker](https://toolbox.vishnudigital.com/upi-qr/milestone-tracker) — Break a freelance project into payment milestones with per-milestone UPI QR codes and a paid/pending progress bar.
* [AMC / Warranty Renewal Reminder with QR](https://toolbox.vishnudigital.com/upi-qr/amc-renewal) — Track annual maintenance contract and warranty renewal dates with a due-status reminder and renewal payment QR.
* [Subscription Bill Reminder Chain with QR](https://toolbox.vishnudigital.com/upi-qr/subscription-reminder) — Track recurring subscription due dates with a countdown status and generate the next cycle's payment QR on demand.
* [Payroll Batch Payslip + QR Generator](https://toolbox.vishnudigital.com/upi-qr/payroll-payslip) — Batch-generate employee payslips with PF/tax deductions and per-employee UPI payment QR codes from a CSV, exported as a ZIP.
* [Instant UPI Pay Link Receiver](https://toolbox.vishnudigital.com/upi-pay) — Generate instant, zero-tracking UPI deep payment intent links for mobile apps.
* [Invoice & Receipt Maker](https://toolbox.vishnudigital.com/invoice) — Create professional GST invoices with embedded UPI payment QR codes, signatures, and PDF download.
* [Digital Business Card & vCard 4.0](https://toolbox.vishnudigital.com/vcard-generator) — Generate RFC 6350 vCard digital business cards with contact QR codes and .vcf downloads.
* [1D Barcode Generator](https://toolbox.vishnudigital.com/barcode-generator) — Generate Code 128, EAN-13, UPC-A, and Code 39 barcodes with scalable SVG and PNG exports.
* [OG Image Social Banner Studio](https://toolbox.vishnudigital.com/og-image) — Design OpenGraph 1200x630 social preview banners with typography presets and batch export.


---

## 📚 Architectural & Downstream Recipes

* [100% Client-Side Privacy Architecture](docs/privacy-architecture.md) — Technical breakdown of WebCrypto sandboxing, CSP policies, and zero server telemetry.
* [Zod Webhook Validation Recipe](docs/recipes/zod-webhook-validation.md) — Protect ingestion boundaries and eliminate schema contract drift.
* [Safe Client-Side JWT Handling Recipe](docs/recipes/safe-jwt-client-handling.md) — Inspect token expiration and claims safely without third-party bloat.
* [cURL to Fetch Integration Recipe](docs/recipes/curl-to-fetch-integration.md) — Transform Chrome DevTools cURL captures into production-grade TypeScript API wrappers.

---

## 💡 Community & Support

* **Feature Requests**: Have a developer utility you'd love to see in Toolbox? [Submit a Tool Request](https://github.com/cooldashing24/toolbox-community/issues/new?template=feature_request.yml).
* **Bug Reports**: Found an edge case with one of our client-side tools? [Open an Issue](https://github.com/cooldashing24/toolbox-community/issues/new?template=bug_report.yml).
* **Security & Vulnerability Disclosure**: Please review our [Security Policy](SECURITY.md) to report vulnerabilities privately.

---

## ⚖️ License & Terms

* Documentation and public integration guides are licensed under [CC-BY-4.0](LICENSE).
* Community integration recipes under `docs/recipes/` are licensed under [MIT](LICENSE).
* The **Toolbox** and **Toolbox Blog** web applications are proprietary, closed-source services maintained by the **[Toolbox Engineering Team](https://toolbox.vishnudigital.com)**.
