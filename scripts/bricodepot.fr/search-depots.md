# Search Brico Depot depots

Automatically search Brico Depot depots on bricodepot.fr. Find Brico Depot depots (stores of bricodepot.fr) by postcode, as the site's depot picker does: the text is matched against the postcodes a depot serves, so a full postcode of the depot's town (92000) or a department prefix (92) works, while an arbitrary city postcode or a city name may match nothing. Returns 5 depots per page with the depot_id to pass to Search Brico Depot products and Get Brico Depot product to get that depot's prices and stock, the name, address, phone and coordinates. An empty list means no depot matches.

- Site: bricodepot.fr
- Address: `reduck/bricodepot.fr/search-depots`
- Updated: 2026-11-24 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/bricodepot.fr/search-depots`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/bricodepot.fr/search-depots
```

## Input

- `postcode` (string, required): Postcode or its first digits, for example 92000 or 92.
- `page` (integer, optional): Result page, 5 depots per page.

## Output

- `page` (integer, required)
- `depots` (array, required)
- `postcode` (string, required)
- `total_pages` (integer | null, required)
- `total_results` (integer | null, required)

## FAQ

### What does "Search Brico Depot depots" do?

Find Brico Depot depots (stores of bricodepot.fr) by postcode, as the site's depot picker does: the text is matched against the postcodes a depot serves, so a full postcode of the depot's town (92000) or a department prefix (92) works, while an arbitrary city postcode or a city name may match nothing. Returns 5 depots per page with the depot_id to pass to Search Brico Depot products and Get Brico Depot product to get that depot's prices and stock, the name, address, phone and coordinates. An empty list means no depot matches.

### How do I automatically search Brico Depot depots on bricodepot.fr?

Ask an AI agent connected to Reduck to run reduck/bricodepot.fr/search-depots, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/bricodepot.fr/search-depots

### Is there a bricodepot.fr API to search Brico Depot depots?

You do not need one. "Search Brico Depot depots" drives the real bricodepot.fr pages in a browser, so it works whether or not bricodepot.fr offers an API for this.

### What information do I need to provide?

Required: postcode. Optional: page.

### What does it return?

It returns page, depots, postcode, total_pages, total_results.

### Do I need to be logged in to bricodepot.fr?

No. It only uses pages of bricodepot.fr that are reachable without signing in.

### Does it change anything on bricodepot.fr, or only read data?

It only reads. It looks things up on bricodepot.fr and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/bricodepot.fr/search-depots, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/bricodepot.fr/search-depots

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/bricodepot.fr/search-depots
