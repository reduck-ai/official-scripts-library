# Get Tripadvisor restaurant details

Automatically get Tripadvisor restaurant details on tripadvisor.com. Fetch a restaurant's Tripadvisor listing: name, cuisine, rating, review count, price range, address, phone, hours, and menu link. No login required.

- Site: tripadvisor.com
- Address: `reduck/tripadvisor.com/get_restaurant`
- Updated: 2026-09-02 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/tripadvisor.com/get_restaurant`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/tripadvisor.com/get_restaurant
```

## Input

- `location_id` (string, required): Tripadvisor restaurant location id, the number after 'd' in the URL, e.g. "14039269" from tripadvisor.com/Restaurant_Review-g187147-d14039269-Reviews-...

## Output

- `available` (boolean, required)
- `location_id` (string, required)
- `url` (string | null, optional)
- `name` (string | null, optional)
- `phone` (string | null, optional)
- `menuUrl` (string | null, optional)
- `cuisines` (array, optional)
- `imageUrl` (string | null, optional)
- `latitude` (number | null, optional)
- `longitude` (number | null, optional)
- `postalCode` (string | null, optional)
- `priceRange` (string | null, optional)
- `ratingValue` (number | null, optional)
- `reviewCount` (integer | null, optional)
- `openingHours` (array, optional)
- `addressRegion` (string | null, optional)
- `streetAddress` (string | null, optional)
- `addressCountry` (string | null, optional)
- `addressLocality` (string | null, optional)

## FAQ

### What does "Get Tripadvisor restaurant details" do?

Fetch a restaurant's Tripadvisor listing: name, cuisine, rating, review count, price range, address, phone, hours, and menu link. No login required.

### How do I automatically get Tripadvisor restaurant details on tripadvisor.com?

Ask an AI agent connected to Reduck to run reduck/tripadvisor.com/get_restaurant, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/tripadvisor.com/get_restaurant

### Is there a tripadvisor.com API to get Tripadvisor restaurant details?

You do not need one. "Get Tripadvisor restaurant details" drives the real tripadvisor.com pages in a browser, so it works whether or not tripadvisor.com offers an API for this.

### What information do I need to provide?

Required: location_id.

### What does it return?

It returns url, name, phone, menuUrl, cuisines, imageUrl, latitude, available, longitude, postalCode, priceRange, location_id, ratingValue, reviewCount, openingHours, addressRegion, streetAddress, addressCountry, addressLocality.

### Do I need to be logged in to tripadvisor.com?

No. It only uses pages of tripadvisor.com that are reachable without signing in.

### Does it change anything on tripadvisor.com, or only read data?

It only reads. It looks things up on tripadvisor.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/tripadvisor.com/get_restaurant, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/tripadvisor.com/get_restaurant

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/tripadvisor.com/get_restaurant
