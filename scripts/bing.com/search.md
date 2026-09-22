# Bing search

Search the web on Bing and return the page's organic result cards (title, url, snippet, age), paging by offset. Bing's /ck/a redirect wrapper is decoded, so urls are the real destination. Anonymous — no login.

- Site: bing.com
- Address: `reduck/bing.com/search`
- Updated: 2026-08-17 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/bing.com/search`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/bing.com/search
```

## Input

- `query` (string, required): The search query. Plain text works; site: is refused by Bing with a bot challenge and quoted phrases are relaxed rather than enforced (see the script description).
- `offset` (integer, optional): Result page, 0 = first (mapped to Bing's &first=offset*10+1), mirroring the SERP pager. Adjacent pages were measured disjoint, so different offsets may be fetched concurrently and unioned; dedupe by url.

## Output

- `count` (integer, required): Number of organic cards on this page. Typically 2-10 and it varies by query: ads and answer blocks share the result list, so a heavily monetised query leaves fewer organic slots. Not a cap the caller can raise.
- `query` (string, required): The query as passed, echoed back.
- `offset` (integer, required): The page that was fetched, echoed back.
- `results` (array, required): The organic result cards on this page, in the order Bing ranked them. Excludes ads, answer panels and video/news blocks, which live in the same list under different classes. Read from the DOM text rather than the rendered layout, so cards stay complete even when Bing collapses the list behind a Copilot answer panel.

## FAQ

### What does "Bing search" do?

Search the web on Bing and return the page's organic result cards (title, url, snippet, age), paging by offset. Bing's /ck/a redirect wrapper is decoded, so urls are the real destination. Anonymous — no login.

### What information do I need to provide?

Required: query. Optional: offset.

### What does it return?

It returns count, query, offset, results.

### Do I need to be logged in to bing.com?

No. It only uses pages of bing.com that are reachable without signing in.

### Does it change anything on bing.com, or only read data?

It only reads. It looks things up on bing.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/bing.com/search, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/bing.com/search

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/bing.com/search
