# Skim — Cursor Plugin

Read any webpage as clean Markdown inside Cursor — **~4x smaller than raw HTML**, so your model gets more signal with fewer tokens. One tool call, no browser, no scraping setup.

## Install

In Cursor, run:

```
/add-plugin skim-mcp
```

Or go to **Settings → Plugins** and search for **Skim**.

## Setup

### Option A — Card API key (recommended)

Get a free key at [skim402.com/pricing](https://skim402.com/pricing) (1,000 reads/month), then add it to Cursor's MCP environment:

```json
{
  "mcpServers": {
    "skim": {
      "command": "npx",
      "args": ["-y", "skim-mcp"],
      "env": {
        "SKIM_API_KEY": "sk402_your_key_here"
      }
    }
  }
}
```

### Option B — Crypto wallet (pay per call)

If you prefer x402 pay-per-call ($0.002 USDC on Base, no monthly plan):

```json
"env": {
  "SKIM_WALLET_PRIVATE_KEY": "0xyour-base-wallet-key"
}
```

Fund the wallet with a small USDC balance on Base. Setup guide: [skim402.com/wallet](https://skim402.com/wallet).

## Tools

| Tool | What it does | Cost |
|------|-------------|------|
| `skim_read` | Read a URL → clean Markdown | $0.002 |
| `skim_extract` | Extract structured fields from a page | $0.005 |
| `skim_search` | Search + read top results | $0.015 |

## Links

- [skim402.com](https://skim402.com) — home page & pricing
- [npm: skim-mcp](https://www.npmjs.com/package/skim-mcp) — package
- [MCP Registry](https://registry.modelcontextprotocol.io) — official listing
