# Etsy get listing

Reads an Etsy listing's title, description, images, price, availability, rating and shop from its public product page.

- Site: etsy.com
- Address: `reduck/etsy.com/get_listing`
- Updated: 2026-09-18 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/etsy.com/get_listing`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/etsy.com/get_listing
```

## Input

- `listing` (string, required): An Etsy listing ID (e.g. "993944520") or any Etsy listing URL containing one (e.g. https://www.etsy.com/listing/993944520/some-slug).

## Output

- `found` (boolean, required)
- `id` (string | null, optional)
- `url` (string | null, optional)
- `name` (string | null, optional)
- `price` (number | null, optional)
- `images` (array, optional)
- `rating` (number | null, optional)
- `shopUrl` (string | null, optional)
- `category` (array, optional)
- `currency` (string | null, optional)
- `material` (string | null, optional)
- `shopName` (string | null, optional)
- `listPrice` (number | null, optional)
- `description` (string | null, optional)
- `reviewCount` (integer | null, optional)
- `availability` (string | null, optional)
- `freeShipping` (boolean | null, optional)
- `shipsFromCountry` (string | null, optional)

## FAQ

### What does "Etsy get listing" do?

Reads an Etsy listing's title, description, images, price, availability, rating and shop from its public product page.

### What information do I need to provide?

Required: listing.

### What does it return?

It returns id, url, name, found, price, images, rating, shopUrl, category, currency, material, shopName, listPrice, description, reviewCount, availability, freeShipping, shipsFromCountry.

### Do I need to be logged in to etsy.com?

No. It only uses pages of etsy.com that are reachable without signing in.

### Does it change anything on etsy.com, or only read data?

It only reads. It looks things up on etsy.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/etsy.com/get_listing, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/etsy.com/get_listing

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/etsy.com/get_listing
