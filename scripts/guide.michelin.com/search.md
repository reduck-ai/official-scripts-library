# Search MICHELIN Guide restaurants

Automatically search MICHELIN Guide restaurants on guide.michelin.com. Search the MICHELIN Guide for restaurants in a given locality (city), optionally filtered by distinction (1/2/3 Stars, Bib Gourmand, or Plate). Resolves the locality name to the Guide's city slug, then reads the site's own restaurant index. Returns the total count and one page of restaurants (name, award, green star, cuisines, price, address, chef, coords, absolute URL, image). Paginate with `page`/`hitsPerPage`. Observation only.

- Site: guide.michelin.com
- Address: `reduck/guide.michelin.com/search`
- Updated: 2026-09-03 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/guide.michelin.com/search`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/guide.michelin.com/search
```

## Input

- `location` (string, required): City / locality name as a caller would type it, e.g. "Lyon", "Paris", "Nice". Resolved to the Guide's city slug via a faceted lookup (the most frequent matching city wins).
- `page` (integer, optional): Zero-based page index. Loop 0..nbPages-1 to fetch everything.
- `award` (string, optional): Optional MICHELIN distinction to filter on. Friendly keys: "1-star", "2-stars", "3-stars", "bib-gourmand", "plate". Raw distinction slugs are also accepted (1-etoile-michelin, 2-etoiles-michelin, 3-etoiles-michelin, bib-gourmand, assiette-michelin). Omit to return all listed restaurants in the locality regardless of distinction.
- `hitsPerPage` (integer, optional): Results per page (max 100).

## Output

- `page` (integer, required)
- `total` (integer, required)
- `nbPages` (integer, required)
- `hitsPerPage` (integer, required)
- `restaurants` (array, required)
- `resolvedCity` (object, required)
- `distinctionSlug` (string | null, optional)

## FAQ

### What does "Search MICHELIN Guide restaurants" do?

Search the MICHELIN Guide for restaurants in a given locality (city), optionally filtered by distinction (1/2/3 Stars, Bib Gourmand, or Plate). Resolves the locality name to the Guide's city slug, then reads the site's own restaurant index. Returns the total count and one page of restaurants (name, award, green star, cuisines, price, address, chef, coords, absolute URL, image). Paginate with `page`/`hitsPerPage`. Observation only.

### How do I automatically search MICHELIN Guide restaurants on guide.michelin.com?

Ask an AI agent connected to Reduck to run reduck/guide.michelin.com/search, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/guide.michelin.com/search

### Is there a guide.michelin.com API to search MICHELIN Guide restaurants?

You do not need one. "Search MICHELIN Guide restaurants" drives the real guide.michelin.com pages in a browser, so it works whether or not guide.michelin.com offers an API for this.

### What information do I need to provide?

Required: location. Optional: page, award, hitsPerPage.

### What does it return?

It returns page, total, nbPages, hitsPerPage, restaurants, resolvedCity, distinctionSlug.

### Do I need to be logged in to guide.michelin.com?

No. It only uses pages of guide.michelin.com that are reachable without signing in.

### Does it change anything on guide.michelin.com, or only read data?

It only reads. It looks things up on guide.michelin.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/guide.michelin.com/search, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/guide.michelin.com/search

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/guide.michelin.com/search
