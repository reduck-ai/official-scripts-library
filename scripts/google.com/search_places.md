# Search Google Maps places

Automatically search Google Maps places on google.com. Search Google Maps for places, optionally near a location, and get the list Maps shows, in its order: name, address, phone, website, main category and all categories, star rating, number of reviews, price range, coordinates and the Google place id. Use the place id with get_place for the opening hours and with get_place_reviews for the reviews. Google Maps lists at most 120 places for one search; complete is true when that list ended, false when cap stopped it first. A precise query that Maps opens as one place returns that one place. Category names follow hl, or the browser's language when hl is empty.

- Site: google.com
- Address: `reduck/google.com/search_places`
- Updated: 2026-10-20 (v7)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/google.com/search_places`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/google.com/search_places
```

## Input

- `query` (string, required): What to search for, as typed in the Maps search box (e.g. 'tattoo artist', 'pizzeria', 'dentist near me').
- `gl` (string, optional): Region that Maps ranks the results for (e.g. 'fr', 'us'). Empty: the browser's region.
- `hl` (string, optional): Language of the category names (e.g. 'en', 'fr'). Empty: the browser's language.
- `cap` (number, optional): How many places to return at most. Google Maps lists at most 120 places for one search.
- `location` (string, optional): Optional place added after the query (e.g. 'Paris', 'Brooklyn'). Without it, Maps searches around the browser's own location.

## Output

- `n` (number, required): Number of places returned.
- `records` (array, required)
- `complete` (boolean, required): true when Maps has no more places for this search (its list ended, or reached its limit of 120). false when cap stopped the list first.

## FAQ

### What does "Search Google Maps places" do?

Search Google Maps for places, optionally near a location, and get the list Maps shows, in its order: name, address, phone, website, main category and all categories, star rating, number of reviews, price range, coordinates and the Google place id. Use the place id with get_place for the opening hours and with get_place_reviews for the reviews. Google Maps lists at most 120 places for one search; complete is true when that list ended, false when cap stopped it first. A precise query that Maps opens as one place returns that one place. Category names follow hl, or the browser's language when hl is empty.

### How do I automatically search Google Maps places on google.com?

Ask an AI agent connected to Reduck to run reduck/google.com/search_places, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/google.com/search_places

### Is there a google.com API to search Google Maps places?

You do not need one. "Search Google Maps places" drives the real google.com pages in a browser, so it works whether or not google.com offers an API for this.

### What information do I need to provide?

Required: query. Optional: gl, hl, cap, location.

### What does it return?

It returns n, records, complete.

### Do I need to be logged in to google.com?

No. It only uses pages of google.com that are reachable without signing in.

### Does it change anything on google.com, or only read data?

It only reads. It looks things up on google.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/google.com/search_places, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/google.com/search_places

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/google.com/search_places
