# Maps: Search Businesses

Automatically search Businesses on google.com. Search for businesses on Google Maps (anonymous, no login): name, category, address, phone, website, rating, reviews, GPS, place_id. Paginates via scrolling, controlled by the count argument.

- Site: google.com
- Address: `reduck/google.com/maps_search_businesses`
- Updated: 2026-08-25 (v5)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/google.com/maps_search_businesses`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/google.com/maps_search_businesses
```

## Input

- `query` (string, required): Natural-language search query, include the geographic area in the query. E.g. 'plumber Paris 2nd arrondissement', 'Italian restaurant Lyon', 'real estate agency Bordeaux'
- `count` (integer, optional): Max number of results to collect (auto-scrolls the results panel; Google caps out around ~120)
- `locale` (string, optional): Optional: force the Google Maps UI to a specific language (Google's own hl= override). Omit to use whatever language the calling browser/account already renders. Only these 5 languages are supported for parsing - the script detects the language actually rendered and throws explicitly if it's not one of these 5, rather than silently returning wrong data.

## Output

- `endOfList` (boolean, required): true if Google stopped producing new results before reaching count, either because it showed an explicit end-of-list marker or because the feed's card count and height both stayed unchanged across a retry window (Google sometimes stops loading more results without ever rendering the end-of-list text, e.g. after silently widening the search radius)
- `businesses` (array, required)
- `resultType` (string, required): 'single' = the query was precise enough that Google redirected straight to the business's own page

## FAQ

### What does "Maps: Search Businesses" do?

Search for businesses on Google Maps (anonymous, no login): name, category, address, phone, website, rating, reviews, GPS, place_id. Paginates via scrolling, controlled by the count argument.

### How do I automatically search Businesses on google.com?

Ask an AI agent connected to Reduck to run reduck/google.com/maps_search_businesses, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/google.com/maps_search_businesses

### Is there a google.com API to search Businesses?

You do not need one. "Maps: Search Businesses" drives the real google.com pages in a browser, so it works whether or not google.com offers an API for this.

### What information do I need to provide?

Required: query. Optional: count, locale.

### What does it return?

It returns endOfList, businesses, resultType.

### Do I need to be logged in to google.com?

No. It only uses pages of google.com that are reachable without signing in.

### Does it change anything on google.com, or only read data?

It only reads. It looks things up on google.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/google.com/maps_search_businesses, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/google.com/maps_search_businesses

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/google.com/maps_search_businesses
