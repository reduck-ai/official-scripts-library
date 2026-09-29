# Raycast — search Store extensions

Automatically search Store extensions on raycast.com. Search the Raycast Store for extensions by keyword: each result's id, slug, title, description, Store URL, author handle and name, download count, supported platforms (macOS / Windows), categories and creation date. Public data, no sign-in needed. A search with no matches returns an empty list.

- Site: raycast.com
- Address: `reduck/raycast.com/search_extensions`
- Updated: 2026-09-28 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/raycast.com/search_extensions`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/raycast.com/search_extensions
```

## Input

- `query` (string, required): Search text, e.g. "github".
- `limit` (integer, optional): Maximum extensions to return (default 20).

## Output

- `count` (integer, required)
- `query` (string, required)
- `extensions` (array, required)

## FAQ

### What does "Raycast — search Store extensions" do?

Search the Raycast Store for extensions by keyword: each result's id, slug, title, description, Store URL, author handle and name, download count, supported platforms (macOS / Windows), categories and creation date. Public data, no sign-in needed. A search with no matches returns an empty list.

### How do I automatically search Store extensions on raycast.com?

Ask an AI agent connected to Reduck to run reduck/raycast.com/search_extensions, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/raycast.com/search_extensions

### Is there a raycast.com API to search Store extensions?

You do not need one. "Raycast — search Store extensions" drives the real raycast.com pages in a browser, so it works whether or not raycast.com offers an API for this.

### What information do I need to provide?

Required: query. Optional: limit.

### What does it return?

It returns count, query, extensions.

### Do I need to be logged in to raycast.com?

No. It only uses pages of raycast.com that are reachable without signing in.

### Does it change anything on raycast.com, or only read data?

It only reads. It looks things up on raycast.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/raycast.com/search_extensions, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/raycast.com/search_extensions

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/raycast.com/search_extensions
