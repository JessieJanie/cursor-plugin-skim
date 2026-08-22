---
name: web-reading
description: When and how to use Skim to read web pages for the user.
---

# Web Reading with Skim

Use the `skim_read` tool whenever you need to fetch or reference live web content — documentation, articles, product pages, search results, or any URL the user provides.

## When to use Skim

- The user pastes or mentions a URL and wants its content summarized or referenced.
- You need up-to-date information from a specific page (pricing, changelogs, docs).
- A task requires reading multiple pages in sequence (research, comparison, audits).
- The user asks you to "check", "read", "summarize", or "look at" a URL.

## How to use it

```
skim_read(url: "https://example.com/page")
```

The response is clean Markdown: body text only, no scripts, no nav, no ads.

## Tips

- Skim works on most public pages without any credentials.
- For paywalled or JS-heavy pages, the response will note the limitation.
- Pass `max_length` to cap output when you only need a summary.
- Chain multiple `skim_read` calls for multi-page research without hitting context limits.

## Payment

Skim uses a card API key (`SKIM_API_KEY`) or x402 pay-per-call via Base USDC. Both paths are configured in your MCP environment — you do not need to manage payments in your prompts.
