# Contributing to the Toolbox Community Hub

Thank you for your interest in contributing to the **Toolbox Community Hub & Developer Reference**! 

Toolbox ([https://toolbox.vishnudigital.com](https://toolbox.vishnudigital.com)) is a **closed-source, proprietary web platform** committed to providing 100% client-side, zero-telemetry utilities running directly in browser memory. 

This repository serves as the official public directory, issue tracker, and downstream recipe bank.

---

## 🚦 Contribution Rules & Guardrails

### 1. 100% Client-Side RAM Invariant
When proposing new tools or submitting community recipes:
- The utility or transformation must be capable of running **100% client-side** using browser Web APIs (e.g., W3C WebCrypto, Canvas, WebAssembly, or pure JavaScript AST engines).
- We **do not** accept suggestions or designs that require server-side state, remote database storage, or external API telemetry for user payloads.

### 2. Downstream Consumption Only
- Code contributed to `docs/recipes/` must demonstrate **how developers consume the outputs** of Toolbox in their own applications (e.g., consuming generated Zod schemas, converting cURL commands into API clients, inspecting JWTs in-browser).
- Do **not** attempt to reverse-engineer, decompile, or submit PRs containing internal application or engine code from the proprietary `toolbox` application.

### 3. Absolute Privacy Mandate (Rule 0)
- **Zero Real Secrets or PII**: Never post real API keys, production JWT tokens, database connection strings, passwords, or personal identifying information in GitHub issues, PRs, or sample fixtures.
- Always use RFC-compliant sanitized mocks (e.g., `user_123`, `example.com`, `sec_test_abc123`).

---

## How You Can Contribute

### 💡 Requesting a New Tool
Have an idea for a client-side developer utility?
1. Check existing tools on [Toolbox](https://toolbox.vishnudigital.com) and the [Issue Tracker](https://github.com/toolbox/toolbox-community/issues).
2. Open a **[Tool Request](https://github.com/toolbox/toolbox-community/issues/new?template=feature_request.yml)** detailing:
   - The developer friction or production failure it solves.
   - The proposed inputs, options, and outputs.
   - How it can execute 100% in browser RAM.

### 🐛 Reporting Bugs
Found an edge case with a parser, regex engine, or crypto tool?
1. Open a **[Bug Report](https://github.com/toolbox/toolbox-community/issues/new?template=bug_report.yml)**.
2. Include your browser engine, operating system, and a sanitized test payload that reproduces the issue.

### 📝 Submitting a Downstream Recipe
Have a great pattern for integrating Toolbox outputs into Next.js, Express, Go, Python, or Rust?
1. Fork this repository.
2. Create a new markdown recipe in `docs/recipes/<recipe-name>.md`.
3. Adhere to TypeScript or language best practices, including error boundaries and type safety.
4. Open a Pull Request referencing the related tool URL.

---

## Development & Link Verification

Before submitting documentation changes or recipes, verify that all outbound links to tools and engineering guides resolve correctly:

```bash
npx lychee --verbose README.md docs/**/*.md
```

All links must point to verified paths on:
- Web Workbench: `https://toolbox.vishnudigital.com/<slug>`
- Engineering Publication: `https://blog.toolbox.vishnudigital.com/<slug>/`

---

## Community Standards

This project adheres to the [Code of Conduct](CODE_OF_CONDUCT.md). By participating, you are expected to uphold this code. For questions, reach out to **`contact@toolbox.vishnudigital.com`**.
