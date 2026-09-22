# Search Pinterest pins

Automatically search Pinterest pins on pinterest.com. Searches Pinterest pins by keyword and returns the first page of results (id, pin URL, thumbnail/full image, dominant color). Read-only, no login required; Pinterest serves a reduced anonymous result set with no title/description per card. Be aware that a query with no real matches still returns Pinterest's recommended pins rather than an empty list.

- Site: pinterest.com
- Address: `reduck/pinterest.com/search_pins`
- Updated: 2026-09-03 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/pinterest.com/search_pins`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/pinterest.com/search_pins
```

## Input

- `query` (string, required): Search keywords, e.g. "minimalist living room"

## FAQ

### What does "Search Pinterest pins" do?

Searches Pinterest pins by keyword and returns the first page of results (id, pin URL, thumbnail/full image, dominant color). Read-only, no login required; Pinterest serves a reduced anonymous result set with no title/description per card. Be aware that a query with no real matches still returns Pinterest's recommended pins rather than an empty list.

### How do I automatically search Pinterest pins on pinterest.com?

Ask an AI agent connected to Reduck to run reduck/pinterest.com/search_pins, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/pinterest.com/search_pins

### Is there a pinterest.com API to search Pinterest pins?

You do not need one. "Search Pinterest pins" drives the real pinterest.com pages in a browser, so it works whether or not pinterest.com offers an API for this.

### What information do I need to provide?

Required: query.

### Do I need to be logged in to pinterest.com?

No. It only uses pages of pinterest.com that are reachable without signing in.

### Does it change anything on pinterest.com, or only read data?

It only reads. It looks things up on pinterest.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/pinterest.com/search_pins, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/pinterest.com/search_pins

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/pinterest.com/search_pins
