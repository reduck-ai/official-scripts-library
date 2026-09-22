# DuckDuckGo search

Search DuckDuckGo for a query and return up to `count` web results, optionally scoped to a region via `kl`. Returns total, noResults and results (rank, title, url, snippet). `total` counts the distinct results collected before truncation to `count`, so it can exceed results.length. Note that site:, "quotes" and OR are honoured as a hard AND, so an over-constrained query legitimately comes back empty with noResults true.

- Site: duckduckgo.com
- Address: `reduck/duckduckgo.com/search`
- Updated: 2026-09-03 (v6)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/duckduckgo.com/search`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/duckduckgo.com/search
```

## Input

- `query` (string, required): Search query. site:domain/path, "quotes" and OR are honored as a hard AND (Bing index).
- `kl` (string, optional): Region code, e.g. fr-fr (default), us-en, wt-wt (none). fr-fr prioritises fr.linkedin.com profiles. Region only — it does not change which results come back beyond that ranking.
- `count` (integer, optional): Max results to return (loads more via 'More results' clicks). Default 10.

## Output

- `total` (integer, required)
- `results` (array, required)
- `noResults` (boolean, required): true = DuckDuckGo explicitly returned its no-results page (an honest zero, not a block).

## FAQ

### What does "DuckDuckGo search" do?

Search DuckDuckGo for a query and return up to `count` web results, optionally scoped to a region via `kl`. Returns total, noResults and results (rank, title, url, snippet). `total` counts the distinct results collected before truncation to `count`, so it can exceed results.length. Note that site:, "quotes" and OR are honoured as a hard AND, so an over-constrained query legitimately comes back empty with noResults true.

### What information do I need to provide?

Required: query. Optional: kl, count.

### What does it return?

It returns total, results, noResults.

### Do I need to be logged in to duckduckgo.com?

No. It only uses pages of duckduckgo.com that are reachable without signing in.

### Does it change anything on duckduckgo.com, or only read data?

It only reads. It looks things up on duckduckgo.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/duckduckgo.com/search, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/duckduckgo.com/search

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/duckduckgo.com/search
