# Skim — Cursor Plugin

Read any webpage as clean Markdown inside Cursor — **~4x smaller than raw HTML**, so your model gets more signal with fewer tokens. One local MCP server, no browser automation, and no scraping setup.

## Install

After approval, install **Skim — Clean Web Reader** from Cursor's official Marketplace. Cursor will ask for your Skim API key when you configure the plugin.

For local testing before Marketplace approval, install this repository as a local Cursor plugin and use the configuration below.

## Setup

### Card API key

Get a free key at [skim402.com/pricing](https://skim402.com/pricing) (1,000 reads/month). The official plugin configuration passes the key to the local MCP process without putting the value in this repository:

```json
{
  "mcpServers": {
    "skim": {
      "command": "npx",
      "args": ["-y", "skim-mcp@0.2.5"],
      "env": {
        "SKIM_API_KEY": "sk402_your_key_here"
      }
    }
  }
}
```

This first-party Cursor plugin intentionally does not ask for a wallet or private key. Wallet/x402 setup remains a separate Skim path.

## Tools

| Tool | What it does | Cost |
|------|-------------|------|
| `skim_read` | Read a URL → clean Markdown | Uses Skim plan credits |
| `skim_extract` | Extract structured fields from a page | Uses Skim plan credits |
| `skim_search` | Search + read top results | Uses Skim plan credits |

## Links

- [skim402.com](https://skim402.com) — home page & pricing
- [Skim docs](https://skim402.com/docs) — API and MCP setup
- [npm: skim-mcp](https://www.npmjs.com/package/skim-mcp) — package
- [MCP Registry](https://registry.modelcontextprotocol.io) — official listing
