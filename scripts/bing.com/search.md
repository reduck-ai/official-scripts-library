# Bing search

Search the web on Bing, one page of results at a time. Returns each organic result's title, url, snippet and date, the market Bing answered for, and where the next page starts.

- Site: bing.com
- Address: `reduck/bing.com/search`
- Updated: 2026-09-24 (v8)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/bing.com/search`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/bing.com/search
```

## Input

- `query` (string, required): The search query. site: is not supported (Bing answers it with a human-verification challenge and the script fails); quoted phrases are loosened by Bing, not enforced.
- `first` (integer, optional): Which page to read, as Bing addresses it: the position of its first result. Pages vary in size, so pass the `next` of the previous answer rather than computing it. Default 1.

## Output

- `next` (integer | null, required): The `first` of the next page; null on the last page. Consecutive pages can repeat a result, so dedupe by url.
- `count` (integer, required): How many organic results this page holds (results.length), typically 2-10.
- `first` (integer, required)
- `query` (string, required)
- `market` (string | null, required): The market Bing answered for, e.g. "en-US", which follows where the browser is; null if the page does not say.
- `hasMore` (boolean, required)
- `results` (array, required): The organic results, in Bing's order. Ads, answer boxes and video carousels are left out.
- `rewrittenTo` (string | null, required): The query Bing searched instead, when it says so ('These are results for …'); else null.
- `emptyBecause` (string | null, required): Bing's reason when `results` is empty; null otherwise.

## FAQ

### What does "Bing search" do?

Search the web on Bing, one page of results at a time. Returns each organic result's title, url, snippet and date, the market Bing answered for, and where the next page starts.

### What information do I need to provide?

Required: query. Optional: first.

### What does it return?

It returns next, count, first, query, market, hasMore, results, rewrittenTo, emptyBecause.

### Do I need to be logged in to bing.com?

No. It only uses pages of bing.com that are reachable without signing in.

### Does it change anything on bing.com, or only read data?

It only reads. It looks things up on bing.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/bing.com/search, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/bing.com/search

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/bing.com/search
