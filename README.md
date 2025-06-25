# @sequenxa/eslint-config

> **Secure ESLint + Prettier configuration for trust-grade TypeScript, React, and Tailwind apps.**  
> Designed for identity systems, AI workflows, and sensitive data platforms. Maintained by [Sequenxa](https://sequenxa.com).

[![npm version](https://img.shields.io/npm/v/@sequenxa/eslint-config.svg?style=flat-square)](https://www.npmjs.com/package/@sequenxa/eslint-config)
[![license](https://img.shields.io/npm/l/@sequenxa/eslint-config.svg?style=flat-square)](./LICENSE)
[![Security Rating](https://img.shields.io/badge/security-hardened-green?style=flat-square)](#security)

---

## 🔍 Why Sequenxa’s Config?

This configuration enforces:
- Type-safe, AI-aware TypeScript
- Secure patterns for identity and verification platforms
- React and Next.js standards
- Tailwind support with zero friction
- Opinionated Prettier formatting
- Prohibited risky constructs like `eval`, `Function`, and `dangerousInnerHTML`

It is actively used and maintained by [Sequenxa](https://sequenxa.com), a leader in AI-powered verification and trust infrastructure.

---

## Installation

```bash
npm install --save-dev @sequenxa/eslint-config
````

Also ensure the required peer dependencies are installed:

```bash
npm install --save-dev \
  eslint \
  prettier \
  eslint-plugin-react \
  eslint-plugin-security \
  @typescript-eslint/eslint-plugin \
  @typescript-eslint/parser \
  eslint-plugin-tailwindcss
```

---

## Usage

Add to your `.eslintrc` config:

```json
{
  "extends": ["@sequenxa/eslint-config"]
}
```

For React projects:

```json
{
  "extends": ["@sequenxa/eslint-config/react"]
}
```

For Tailwind projects:

```json
{
  "extends": ["@sequenxa/eslint-config/tailwind"]
}
```

For all-in-one setups:

```json
{
  "extends": [
    "@sequenxa/eslint-config/react",
    "@sequenxa/eslint-config/tailwind"
  ]
}
```

Prettier is automatically compatible if you add:

```json
{
  "singleQuote": true,
  "trailingComma": "es5"
}
```

---

## Testing

You can test this config against sample files using:

```bash
npm run test
```

Example test config is included in `.eslintrc.example.json`.

---

## Security Notes

This config enforces:

* No use of `eval` or `Function` constructors
* Disallows `dangerouslySetInnerHTML` unless explicitly overridden
* Encourages strict type safety boundaries in AI-powered code

If you are building applications involving consent, compliance, or data integrity — these settings align with best practices for high-assurance environments.

---

## Included Rule Layers

| Config File          | Description                                           |
| -------------------- | ----------------------------------------------------- |
| `index.js`           | Core secure TypeScript + Prettier baseline            |
| `react.js`           | React + JSX rules (with `eslint-plugin-react`)        |
| `tailwind.js`        | Tailwind-specific rules (`eslint-plugin-tailwindcss`) |
| `prettier.config.js` | Shared formatting config                              |

---

## Who’s This For?

This config is for:

* Developers working on sensitive apps (identity, healthcare, legal, verification)
* AI-first teams needing stricter safety patterns
* Organizations building secure, compliant frontends
* Any project under the Sequenxa ecosystem

---

## About Sequenxa

Sequenxa is an AI-powered trust infrastructure platform for governments, enterprises, and high-assurance organizations.
We build verification systems for background checks, consent workflows, and digital evidence systems.

Learn more at [sequenxa.com](https://sequenxa.com)

---

## License

MIT — see [LICENSE](./LICENSE)

---

```
