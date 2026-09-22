# Search Medium articles

Automatically search Medium articles on medium.com. Search Medium for articles by keyword: title, URL, author, publication, tags, claps, read time, and whether the article is locked (member-only). No login required.

- Site: medium.com
- Address: `reduck/medium.com/search`
- Updated: 2026-09-02 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/medium.com/search`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/medium.com/search
```

## Input

- `query` (string, required): Search keywords, e.g. "obsidian productivity"

## Output

- `query` (string, required)
- `results` (array, required)

## FAQ

### What does "Search Medium articles" do?

Search Medium for articles by keyword: title, URL, author, publication, tags, claps, read time, and whether the article is locked (member-only). No login required.

### How do I automatically search Medium articles on medium.com?

Ask an AI agent connected to Reduck to run reduck/medium.com/search, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/medium.com/search

### Is there a medium.com API to search Medium articles?

You do not need one. "Search Medium articles" drives the real medium.com pages in a browser, so it works whether or not medium.com offers an API for this.

### What information do I need to provide?

Required: query.

### What does it return?

It returns query, results.

### Do I need to be logged in to medium.com?

No. It only uses pages of medium.com that are reachable without signing in.

### Does it change anything on medium.com, or only read data?

It only reads. It looks things up on medium.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/medium.com/search, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/medium.com/search

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/medium.com/search
