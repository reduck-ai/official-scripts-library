# Get Leboncoin ad

Automatically get Leboncoin ad on leboncoin.fr. Fetch a single Leboncoin classified ad by its URL. Returns title, full description, price, seller info, location, favorites count, all images, and a generic list of the ad's own category-specific attributes (e.g. mileage/fuel for a car, rooms/surface for a real estate listing, condition/material for furniture) with their labels and values as leboncoin itself displays them. Works across every category since the attribute list is read generically rather than assuming a fixed schema per category.

- Site: leboncoin.fr
- Address: `reduck/leboncoin.fr/get_ad`
- Updated: 2026-09-14 (v4)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/leboncoin.fr/get_ad`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/leboncoin.fr/get_ad
```

## Input

- `url` (string, required): Full Leboncoin ad URL, e.g. 'https://www.leboncoin.fr/ad/voitures/1234567890' (as returned by the search script's ads[].url).

## Output

- `id` (string, required)
- `url` (string, required)
- `title` (string | null, required)
- `images` (array, required)
- `attributes` (array, required)
- `lat` (number | null, optional)
- `lng` (number | null, optional)
- `city` (string | null, optional)
- `zipcode` (string | null, optional)
- `currency` (string | null, optional)
- `has_phone` (boolean, optional)
- `price_eur` (number | null, optional)
- `category_id` (string | null, optional)
- `description` (string | null, optional)
- `image_count` (integer, optional)
- `region_name` (string | null, optional)
- `seller_name` (string | null, optional)
- `seller_type` (string | null, optional)
- `published_at` (string | null, optional)
- `category_name` (string | null, optional)
- `department_name` (string | null, optional)
- `favorites_count` (number | null, optional)
- `seller_profile_url` (string | null, optional)

## FAQ

### What does "Get Leboncoin ad" do?

Fetch a single Leboncoin classified ad by its URL. Returns title, full description, price, seller info, location, favorites count, all images, and a generic list of the ad's own category-specific attributes (e.g. mileage/fuel for a car, rooms/surface for a real estate listing, condition/material for furniture) with their labels and values as leboncoin itself displays them. Works across every category since the attribute list is read generically rather than assuming a fixed schema per category.

### How do I automatically get Leboncoin ad on leboncoin.fr?

Ask an AI agent connected to Reduck to run reduck/leboncoin.fr/get_ad, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/leboncoin.fr/get_ad

### Is there a leboncoin.fr API to get Leboncoin ad?

You do not need one. "Get Leboncoin ad" drives the real leboncoin.fr pages in a browser, so it works whether or not leboncoin.fr offers an API for this.

### What information do I need to provide?

Required: url.

### What does it return?

It returns id, lat, lng, url, city, title, images, zipcode, currency, has_phone, price_eur, attributes, category_id, description, image_count, region_name, seller_name, seller_type, published_at, category_name, department_name, favorites_count, seller_profile_url.

### Do I need to be logged in to leboncoin.fr?

No. It only uses pages of leboncoin.fr that are reachable without signing in.

### Does it change anything on leboncoin.fr, or only read data?

It only reads. It looks things up on leboncoin.fr and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/leboncoin.fr/get_ad, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/leboncoin.fr/get_ad

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/leboncoin.fr/get_ad
