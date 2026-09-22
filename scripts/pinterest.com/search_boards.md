# Search Pinterest boards

Automatically search Pinterest boards on pinterest.com. Searches Pinterest boards by keyword and returns the first page of results (name, url, pin count, cover images, owner). Read-only, no login required; Pinterest serves a reduced anonymous result set.

- Site: pinterest.com
- Address: `reduck/pinterest.com/search_boards`
- Updated: 2026-09-03 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/pinterest.com/search_boards`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/pinterest.com/search_boards
```

## Input

- `query` (string, required): Search keywords, e.g. "minimalist living room"

## FAQ

### What does "Search Pinterest boards" do?

Searches Pinterest boards by keyword and returns the first page of results (name, url, pin count, cover images, owner). Read-only, no login required; Pinterest serves a reduced anonymous result set.

### How do I automatically search Pinterest boards on pinterest.com?

Ask an AI agent connected to Reduck to run reduck/pinterest.com/search_boards, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/pinterest.com/search_boards

### Is there a pinterest.com API to search Pinterest boards?

You do not need one. "Search Pinterest boards" drives the real pinterest.com pages in a browser, so it works whether or not pinterest.com offers an API for this.

### What information do I need to provide?

Required: query.

### Do I need to be logged in to pinterest.com?

No. It only uses pages of pinterest.com that are reachable without signing in.

### Does it change anything on pinterest.com, or only read data?

It only reads. It looks things up on pinterest.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/pinterest.com/search_boards, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/pinterest.com/search_boards

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/pinterest.com/search_boards
