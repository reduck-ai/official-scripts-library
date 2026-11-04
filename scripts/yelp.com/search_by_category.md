# Browse Yelp businesses by category

Automatically browse Yelp businesses by category on yelp.com. Browse Yelp businesses in a specific category (e.g. 'pizza', 'plumbing') and location, using Yelp's category filter rather than free-text search. Returns matching businesses with name, url, rating, review count, price range, and categories.

- Site: yelp.com
- Address: `reduck/yelp.com/search_by_category`
- Updated: 2026-11-03 (v5)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/yelp.com/search_by_category`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/yelp.com/search_by_category
```

## Input

- `category` (string, required): Yelp category alias, e.g. 'pizza', 'plumbing', 'coffee'
- `location` (string, required): Location, e.g. 'New York, NY'
- `start` (integer, optional): Offset of the first result, in steps of 10 (Yelp shows 10 per page). Use nextStart from a previous run.

## Output

- `count` (integer, required)
- `category` (string, required)
- `location` (string, required)
- `businesses` (array, required)
- `start` (integer, optional)
- `nextStart` (integer | null, optional): Pass as start for the next page; null on the last page.
- `totalResults` (integer | null, optional)

## FAQ

### What does "Browse Yelp businesses by category" do?

Browse Yelp businesses in a specific category (e.g. 'pizza', 'plumbing') and location, using Yelp's category filter rather than free-text search. Returns matching businesses with name, url, rating, review count, price range, and categories.

### How do I automatically browse Yelp businesses by category on yelp.com?

Ask an AI agent connected to Reduck to run reduck/yelp.com/search_by_category, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/yelp.com/search_by_category

### Is there a yelp.com API to browse Yelp businesses by category?

You do not need one. "Browse Yelp businesses by category" drives the real yelp.com pages in a browser, so it works whether or not yelp.com offers an API for this.

### What information do I need to provide?

Required: category, location. Optional: start.

### What does it return?

It returns count, start, category, location, nextStart, businesses, totalResults.

### Do I need to be logged in to yelp.com?

No. It only uses pages of yelp.com that are reachable without signing in.

### Does it change anything on yelp.com, or only read data?

It only reads. It looks things up on yelp.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/yelp.com/search_by_category, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/yelp.com/search_by_category

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/yelp.com/search_by_category
