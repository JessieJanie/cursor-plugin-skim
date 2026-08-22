# Skim — Cursor Plugin

Read any webpage as clean Markdown inside Cursor. One tool call, no browser, no scraping setup.

## Install

In Cursor, run:

```
/add-plugin skim-mcp
```

Or go to **Settings → Plugins** and search for **Skim**.

## Setup

No API key is required to start. Skim includes a free tier.

For higher rate limits, add your card API key to Cursor's MCP environment:

```json
{
  "mcpServers": {
    "skim": {
      "command": "npx",
      "args": ["-y", "skim-mcp"],
      "env": {
        "SKIM_API_KEY": "sk-your-key-here"
      }
    }
  }
}
```

Get a free key at [skim402.com/pricing](https://skim402.com/pricing).

## Wallet pay (alternative)

If you prefer pay-per-call via Base USDC instead of a card key:

```json
"env": {
  "SKIM_WALLET_PRIVATE_KEY": "0xyour-base-wallet-key"
}
```

Fund the wallet with a small USDC balance on Base. Each read costs $0.002.

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
