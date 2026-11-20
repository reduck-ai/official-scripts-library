# Search Internet Archive items

Automatically search Internet Archive items on archive.org. Search the Internet Archive catalogue (books, movies, audio, software, web collections) by keywords or advanced query, with optional media type, collection and sort. Returns one page of items with identifier, title, creator, year, media type and download count, plus the total number found. Page through with the page argument; an empty list means nothing matched.

- Site: archive.org
- Address: `reduck/archive.org/search_items`
- Updated: 2026-11-19 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/archive.org/search_items`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/archive.org/search_items
```

## Input

- `query` (string, required): Keywords or an Internet Archive advanced query, e.g. 'title:(moby dick)'.
- `page` (integer, optional)
- `rows` (integer, optional)
- `sort` (string, optional)
- `mediatype` (string, optional): Restrict to one media type.
- `collection` (string, optional): Restrict to a collection identifier, e.g. 'nasa'.

## Output

- `items` (array, required)
- `total` (integer, required)
- `page` (integer, optional)

## FAQ

### What does "Search Internet Archive items" do?

Search the Internet Archive catalogue (books, movies, audio, software, web collections) by keywords or advanced query, with optional media type, collection and sort. Returns one page of items with identifier, title, creator, year, media type and download count, plus the total number found. Page through with the page argument; an empty list means nothing matched.

### How do I automatically search Internet Archive items on archive.org?

Ask an AI agent connected to Reduck to run reduck/archive.org/search_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/archive.org/search_items

### Is there a archive.org API to search Internet Archive items?

You do not need one. "Search Internet Archive items" drives the real archive.org pages in a browser, so it works whether or not archive.org offers an API for this.

### What information do I need to provide?

Required: query. Optional: page, rows, sort, mediatype, collection.

### What does it return?

It returns page, items, total.

### Do I need to be logged in to archive.org?

No. It only uses pages of archive.org that are reachable without signing in.

### Does it change anything on archive.org, or only read data?

It only reads. It looks things up on archive.org and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/archive.org/search_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/archive.org/search_items

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/archive.org/search_items
