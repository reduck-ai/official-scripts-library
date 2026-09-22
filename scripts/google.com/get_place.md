# Get Google Maps place details

Automatically get Google Maps place details on google.com. Get one Google Maps place/business details by placeId (canonical ChIJ... from search_places), place URL, or free-text name+location. Returns name, fullAddress, phone, website, instagram, category, rating, reviews, hours, plusCode, lat, lng, placeId, placeUrl, resolvedUrl, matched, elapsed_s. matched is false when it did not resolve; the free-text path falls back to the first search result, so it can resolve the wrong place. Business fields (rating/reviews/hours/category/lat/lng/plusCode) are null when the place does not expose them.

- Site: google.com
- Address: `reduck/google.com/get_place`
- Updated: 2026-09-17 (v7)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/google.com/get_place`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/google.com/get_place
```

## Input

- `query` (string, optional): Free-text name + location (e.g. 'Casita of Brooklyn'), used only when no placeId/place URL is available; resolves via search + first result.
- `placeId` (string, optional): Canonical Google place ID (e.g. 'ChIJ...'), as returned by search_places. The precise, preferred input.
- `placeUrl` (string, optional): A Google Maps place URL. A '?q=place_id:' or '/data=' URL resolves directly to the place; anything else is treated as free text.
- `settleMs` (number, optional): Milliseconds to wait for the place panel to settle after loading.

## Output

- `lat` (number | null, optional): Latitude parsed from the resolved Maps URL; null when not resolvable.
- `lng` (number | null, optional): Longitude parsed from the resolved Maps URL; null when not resolvable.
- `name` (string | null, optional): Place name. Taken from the detail panel heading, or from the canonical URL when the panel did not render (in which case matched is false).
- `hours` (string | null, optional): Today's opening-hours summary; null when not shown.
- `phone` (string, optional)
- `rating` (number | null, optional): Average Google rating 0-5; null when the place has no rating.
- `matched` (boolean, optional): True only when the place detail panel rendered or a real field (website/phone/address) was read. False means the place did not resolve and the other fields are unreliable.
- `placeId` (string, optional): The placeId actually used (resolved from the arg or the URL; empty on the free-text path).
- `reviews` (integer | null, optional): Google review count, read from the rating header block; null when not shown.
- `website` (string, optional)
- `category` (string | null, optional): Primary Google Maps business category; null when none.
- `placeUrl` (string, optional): Echo of the placeUrl arg.
- `plusCode` (string | null, optional): Google Plus Code (open location code); null when not shown.
- `elapsed_s` (number, optional)
- `instagram` (string, optional): Instagram profile URL when the place links one; empty otherwise.
- `fullAddress` (string, optional)
- `resolvedUrl` (string, optional): Final Maps URL after redirect (the canonical place URL when a place loaded).

## FAQ

### What does "Get Google Maps place details" do?

Get one Google Maps place/business details by placeId (canonical ChIJ... from search_places), place URL, or free-text name+location. Returns name, fullAddress, phone, website, instagram, category, rating, reviews, hours, plusCode, lat, lng, placeId, placeUrl, resolvedUrl, matched, elapsed_s. matched is false when it did not resolve; the free-text path falls back to the first search result, so it can resolve the wrong place. Business fields (rating/reviews/hours/category/lat/lng/plusCode) are null when the place does not expose them.

### How do I automatically get Google Maps place details on google.com?

Ask an AI agent connected to Reduck to run reduck/google.com/get_place, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/google.com/get_place

### Is there a google.com API to get Google Maps place details?

You do not need one. "Get Google Maps place details" drives the real google.com pages in a browser, so it works whether or not google.com offers an API for this.

### What information do I need to provide?

Optional: query, placeId, placeUrl, settleMs.

### What does it return?

It returns lat, lng, name, hours, phone, rating, matched, placeId, reviews, website, category, placeUrl, plusCode, elapsed_s, instagram, fullAddress, resolvedUrl.

### Do I need to be logged in to google.com?

No. It only uses pages of google.com that are reachable without signing in.

### Does it change anything on google.com, or only read data?

It only reads. It looks things up on google.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/google.com/get_place, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/google.com/get_place

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/google.com/get_place
