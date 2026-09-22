# Search Yelp businesses

Automatically search Yelp businesses on yelp.com. Search Yelp businesses by free-text query and location. Returns matching businesses with name, url, rating, review count, price range, and categories.

- Site: yelp.com
- Address: `reduck/yelp.com/search_businesses`
- Updated: 2026-08-17 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/yelp.com/search_businesses`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/yelp.com/search_businesses
```

## Input

- `query` (string, required): Free-text search query, e.g. 'pizza' or 'plumber'
- `location` (string, required): Location, e.g. 'New York, NY'

## Output

- `count` (integer, optional)
- `query` (string, optional)
- `location` (string, optional)
- `businesses` (array, optional)

## FAQ

### What does "Search Yelp businesses" do?

Search Yelp businesses by free-text query and location. Returns matching businesses with name, url, rating, review count, price range, and categories.

### How do I automatically search Yelp businesses on yelp.com?

Ask an AI agent connected to Reduck to run reduck/yelp.com/search_businesses, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/yelp.com/search_businesses

### Is there a yelp.com API to search Yelp businesses?

You do not need one. "Search Yelp businesses" drives the real yelp.com pages in a browser, so it works whether or not yelp.com offers an API for this.

### What information do I need to provide?

Required: query, location.

### What does it return?

It returns count, query, location, businesses.

### Do I need to be logged in to yelp.com?

No. It only uses pages of yelp.com that are reachable without signing in.

### Does it change anything on yelp.com, or only read data?

It only reads. It looks things up on yelp.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/yelp.com/search_businesses, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/yelp.com/search_businesses

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/yelp.com/search_businesses
