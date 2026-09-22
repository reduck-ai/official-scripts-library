# Etsy get shop

Reads an Etsy shop's name, rating, sales, years active, location and featured items from its public storefront page.

- Site: etsy.com
- Address: `reduck/etsy.com/get_shop`
- Updated: 2026-09-18 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/etsy.com/get_shop`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/etsy.com/get_shop
```

## Input

- `shopName` (string, required): The Etsy shop's name as it appears in its URL, e.g. "Walletree" for https://www.etsy.com/shop/Walletree.

## Output

- `found` (boolean, required)
- `url` (string | null, optional)
- `logo` (string | null, optional)
- `name` (string | null, optional)
- `sales` (string | null, optional)
- `banner` (string | null, optional)
- `rating` (number | null, optional)
- `location` (string | null, optional)
- `reviewCount` (integer | null, optional)
- `yearsOnEtsy` (string | null, optional)
- `listingCount` (integer | null, optional)
- `featuredListings` (array, optional)

## FAQ

### What does "Etsy get shop" do?

Reads an Etsy shop's name, rating, sales, years active, location and featured items from its public storefront page.

### What information do I need to provide?

Required: shopName.

### What does it return?

It returns url, logo, name, found, sales, banner, rating, location, reviewCount, yearsOnEtsy, listingCount, featuredListings.

### Do I need to be logged in to etsy.com?

No. It only uses pages of etsy.com that are reachable without signing in.

### Does it change anything on etsy.com, or only read data?

It only reads. It looks things up on etsy.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/etsy.com/get_shop, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/etsy.com/get_shop

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/etsy.com/get_shop
