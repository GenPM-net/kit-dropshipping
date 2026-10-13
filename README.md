# @core/kit-dropshipping

[![genpm](https://api.genpm.net/v1/badge/@core/kit-dropshipping.svg)](https://genpm.net/p/@core/kit-dropshipping) ![license](https://img.shields.io/badge/license-MIT-blue)

> Dropshipping kit for Next.js: supplier import, margin rules, product landings, order forwarding and exceptions

A [GenPM](https://genpm.net) module: **source code + AI rules + MCP config**, injected into your project instead of hidden in `node_modules`. The code lands in `src/app/(dropshipping)`, pinned to a verified commit, and you own it.

## Install

```bash
genpm add @core/kit-dropshipping
```

No genpm yet? `curl -fsSL https://genpm.net/install.sh | sh` (macOS/Linux), `irm https://genpm.net/install.ps1 | iex` (Windows), or one-off with `npx @genpm-net/cli add @core/kit-dropshipping`.

Or let your AI agent do it: run `genpm mcp setup` once, then ask *"add @core/kit-dropshipping with genpm"* in Claude Code, Cursor, VS Code, Windsurf, Codex or Gemini CLI. It shows you a dry-run plan before writing anything.

## What it does

Dropshipping on top of @core/kit-store and @core/kit-landing (kit-cms arrives once through both): connect suppliers,
import products with their cost and a price from margin rules (@core/pricing), single-product landings at `/p/<slug>`
with direct "buy now" to Stripe, automatic or approved forwarding of paid orders to the supplier, tracking sync,
exceptions for what cannot be automated and an estimated profit widget. Logic lives in @core/suppliers and @core/pricing.

## At a glance

- **GenPM dependencies** (installed with it): [@core/kit-store](https://genpm.net/p/@core/kit-store), [@core/kit-landing](https://genpm.net/p/@core/kit-landing), [@core/suppliers](https://genpm.net/p/@core/suppliers), [@core/pricing](https://genpm.net/p/@core/pricing)
- **npm dependencies** (proposed, never installed without asking): `next`, `react`
- **Environment variables** (added to `.env.example`): `PAYMENT_FEE_BPS`, `PAYMENT_FEE_FIXED`, `SUPPLIERS_SYNC_CRON`, `SUPPLIERS_TRACKING_CRON`
- **AI rules**: [`AGENTS.md`](AGENTS.md), loaded by your agent only when it works in `src/app/(dropshipping)`

## Security

GenPM installs a 40-character commit SHA (never a branch), verifies an Ed25519-signed manifest, never runs install scripts and scans AI rules for prompt injection. Details: [genpm.net/docs/security](https://genpm.net/docs/security).

## License

MIT — see [LICENSE](LICENSE). Browse the full catalog at [genpm.net](https://genpm.net).
