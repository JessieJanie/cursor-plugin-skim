# Skim — Cursor Plugin

Skim is more than a simple web reader. This plugin gives Cursor the complete Skim MCP toolkit: clean single and batch reads, JavaScript/browser rendering for dynamic pages, structured extraction, linked-page crawling, PDFs, page-change watches, and curated Signals. Skim's clean Markdown is typically **~4x smaller than raw HTML in measured comparisons**, so the model gets more useful content with less noise.

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

The bundled `skim-mcp` server exposes eight tools:

| Tool | What it does |
|------|--------------|
| `read_url` | Read one URL as clean Markdown |
| `read_urls` | Batch-read several URLs in one request |
| `extract_url` | Extract structured fields using a schema |
| `crawl_url` | Read a page and its linked pages |
| `read_pdf` | Read a public PDF |
| `watch_urls` | Register pages to watch for changes |
| `check_watch` | Poll a watch and return detected changes |
| `poll_signal` | Read a curated Skim Signal feed |

Try the same workflows first in Skim's [Playground](https://skim402.com/playground)
or [Workbench](https://skim402.com/workbench).
## Links

- [skim402.com](https://skim402.com) — home page
- [Pricing and free key](https://skim402.com/pricing) — card-plan setup
- [Playground](https://skim402.com/playground) and [Workbench](https://skim402.com/workbench) — test every workflow
- [Skim docs](https://skim402.com/docs) — API and MCP setup
- [npm: skim-mcp](https://www.npmjs.com/package/skim-mcp) — package
- [MCP Registry](https://registry.modelcontextprotocol.io) — official listing
