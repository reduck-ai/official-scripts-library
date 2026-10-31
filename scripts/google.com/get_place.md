# Get Google Maps place details

Automatically get Google Maps place details on google.com. Get one Google Maps place by its place id (from search_places or get_directions), its Maps link, or a query that names one place. Returns name, address, phone, website, Instagram link, main category and all categories, star rating, number of reviews, price range, the opening hours of the week as numbers in the place's own time zone, plus code, time zone and coordinates (the input of get_directions). A place id or link that Google Maps does not know fails with a clear error. A query that Maps answers with a list of places fails and asks for search_places, rather than picking one of them. Fields a place does not show (phone, website, Instagram, rating, hours and others) are null.

- Site: google.com
- Address: `reduck/google.com/get_place`
- Updated: 2026-10-30 (v11)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/google.com/get_place`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/google.com/get_place
```

## Input

- `gl` (string, optional): Region (e.g. 'fr', 'us'). Empty: the browser's region.
- `hl` (string, optional): Language of the category names (e.g. 'en', 'fr'). Empty: the browser's language.
- `query` (string, optional): Name and location of one place (e.g. 'Café de Flore Paris'). It works only when Maps opens it as one place; a query that Maps answers with a list fails and names search_places.
- `placeId` (string, optional): Google place id (e.g. 'ChIJ...'), as search_places returns it. The preferred input.
- `placeUrl` (string, optional): A Google Maps place link: a '?q=place_id:' link or a '/maps/place/.../data=' link opens that place directly.

## Output

- `name` (string, required)
- `placeId` (string, required): Google place id: the input of get_place_reviews.
- `lat` (number | null, optional)
- `lng` (number | null, optional)
- `phone` (string | null, optional): null when the place has none.
- `price` (string | null, optional)
- `rating` (number | null, optional): Average star rating 1-5; null when the place has no rating.
- `address` (string, optional)
- `reviews` (number | null, optional): Number of reviews; null when the place has none.
- `website` (string | null, optional): null when the place has none.
- `category` (string | null, optional)
- `placeUrl` (string, optional)
- `plusCode` (string | null, optional)
- `timezone` (string | null, optional): IANA time zone of the place, e.g. 'Europe/Paris'.
- `instagram` (string | null, optional): Instagram profile link when the place shows one; null otherwise.
- `categories` (array, optional)
- `resolvedUrl` (string, optional): The Maps URL the place opened at.
- `openingHours` (array | null, optional): The week Maps shows, in the place's own time zone: one entry per opening interval, none for a day it is closed. null when the place shows no hours.

## FAQ

### What does "Get Google Maps place details" do?

Get one Google Maps place by its place id (from search_places or get_directions), its Maps link, or a query that names one place. Returns name, address, phone, website, Instagram link, main category and all categories, star rating, number of reviews, price range, the opening hours of the week as numbers in the place's own time zone, plus code, time zone and coordinates (the input of get_directions). A place id or link that Google Maps does not know fails with a clear error. A query that Maps answers with a list of places fails and asks for search_places, rather than picking one of them. Fields a place does not show (phone, website, Instagram, rating, hours and others) are null.

### How do I automatically get Google Maps place details on google.com?

Ask an AI agent connected to Reduck to run reduck/google.com/get_place, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/google.com/get_place

### Is there a google.com API to get Google Maps place details?

You do not need one. "Get Google Maps place details" drives the real google.com pages in a browser, so it works whether or not google.com offers an API for this.

### What information do I need to provide?

Optional: gl, hl, query, placeId, placeUrl.

### What does it return?

It returns lat, lng, name, phone, price, rating, address, placeId, reviews, website, category, placeUrl, plusCode, timezone, instagram, categories, resolvedUrl, openingHours.

### Do I need to be logged in to google.com?

No. It only uses pages of google.com that are reachable without signing in.

### Does it change anything on google.com, or only read data?

It only reads. It looks things up on google.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/google.com/get_place, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/google.com/get_place

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/google.com/get_place
