# Search eBay listings

Automatically search eBay listings on ebay.com. Search eBay for items by keyword: item id, title, price, currency, shipping cost, location, and seller feedback. No login required.

- Site: ebay.com
- Address: `reduck/ebay.com/search_listings`
- Updated: 2026-09-18 (v4)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/ebay.com/search_listings`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/ebay.com/search_listings
```

## Input

- `query` (string, required): Search keywords, e.g. "vintage camera"

## Output

- `query` (string, required)
- `results` (array, required): Listings eBay returned as matches for the query.
- `returned` (integer, optional): How many matching listings this page yielded, excluding the loosely-related ones.
- `relatedResults` (array, optional): Listings eBay appended when the query ran out of matches. They are not results for the query and are kept apart so they cannot be mistaken for matches; usually empty.
- `resultCountText` (string | null, optional): eBay's own count heading, verbatim ("130,000+ results for vintage camera"). Compare it with `returned`: it is the site's total for the query, while the script reads one page.

## FAQ

### What does "Search eBay listings" do?

Search eBay for items by keyword: item id, title, price, currency, shipping cost, location, and seller feedback. No login required.

### How do I automatically search eBay listings on ebay.com?

Ask an AI agent connected to Reduck to run reduck/ebay.com/search_listings, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/ebay.com/search_listings

### Is there a ebay.com API to search eBay listings?

You do not need one. "Search eBay listings" drives the real ebay.com pages in a browser, so it works whether or not ebay.com offers an API for this.

### What information do I need to provide?

Required: query.

### What does it return?

It returns query, results, returned, relatedResults, resultCountText.

### Do I need to be logged in to ebay.com?

No. It only uses pages of ebay.com that are reachable without signing in.

### Does it change anything on ebay.com, or only read data?

It only reads. It looks things up on ebay.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/ebay.com/search_listings, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/ebay.com/search_listings

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/ebay.com/search_listings
