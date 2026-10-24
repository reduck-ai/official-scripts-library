# Etsy search listings

Searches Etsy listings by keyword and returns every listing on one results page (about 60, ads included as Etsy shows them) with title, link, price, original price when on sale, currency, shop and image, plus Etsy's total match count. Use page to go further. Etsy always suggests near matches, so an empty list is rare; availability is not shown in search results and comes back null.

- Site: etsy.com
- Address: `reduck/etsy.com/search_listings`
- Updated: 2026-10-23 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/etsy.com/search_listings`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/etsy.com/search_listings
```

## Input

- `query` (string, required): Search keywords, e.g. "ceramic mug".
- `page` (integer, optional): Result page, 1-based.
- `digitalDownloads` (string, optional): Whether to exclude instant digital downloads from the results or return only those. Etsy offers no setting that returns both together. Defaults to exclude, which is what Etsy itself applies when the filter is left unset.

## Output

- `page` (integer, required)
- `query` (string, required)
- `results` (array, required)
- `digitalDownloads` (string, required)
- `totalCount` (integer | null, optional)

## FAQ

### What does "Etsy search listings" do?

Searches Etsy listings by keyword and returns every listing on one results page (about 60, ads included as Etsy shows them) with title, link, price, original price when on sale, currency, shop and image, plus Etsy's total match count. Use page to go further. Etsy always suggests near matches, so an empty list is rare; availability is not shown in search results and comes back null.

### What information do I need to provide?

Required: query. Optional: page, digitalDownloads.

### What does it return?

It returns page, query, results, totalCount, digitalDownloads.

### Do I need to be logged in to etsy.com?

No. It only uses pages of etsy.com that are reachable without signing in.

### Does it change anything on etsy.com, or only read data?

It only reads. It looks things up on etsy.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/etsy.com/search_listings, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/etsy.com/search_listings

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/etsy.com/search_listings
