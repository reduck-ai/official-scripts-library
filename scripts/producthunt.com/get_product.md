# Get Product Hunt product

Automatically get Product Hunt product on producthunt.com. Read a Product Hunt product page and return its profile: name, tagline, full description, the outbound website link, the categories it is listed under, its review rating and review count, how many times it has launched, its makers with their Product Hunt profiles, and any Top Product or Golden Kitty awards. Accepts either the product slug or a full Product Hunt product URL. Follower counts are returned exactly as the page displays them (Product Hunt rounds them, e.g. "18K") alongside a numeric approximation. An unknown product is reported as such rather than returned as an empty record.

- Site: producthunt.com
- Address: `reduck/producthunt.com/get_product`
- Updated: 2026-11-06 (v7)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/producthunt.com/get_product`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/producthunt.com/get_product
```

## Input

- `product` (string, required): Product Hunt product slug (e.g. "notion", "raycast") or a full product URL (e.g. "https://www.producthunt.com/products/notion"). Both resolve to the same page.

## Output

- `url` (string, required): Canonical product page URL.
- `name` (string, required)
- `slug` (string, required): The product's slug on Product Hunt.
- `makers` (array, required): People credited on the product, with their Product Hunt profiles. Empty when none are credited.
- `categories` (array, required): Categories linked in the product header, as listed. Empty when none.
- `tagline` (string | null, optional)
- `website` (string | null, optional)
- `productId` (string | null, optional)
- `topProduct` (boolean, optional)
- `description` (string | null, optional)
- `goldenKitty` (boolean, optional)
- `latestAward` (string | null, optional)
- `ratingCount` (number | null, optional)
- `ratingValue` (number | null, optional)
- `datePublished` (string | null, optional)
- `launchesCount` (number | null, optional)
- `followersCount` (number | null, optional): Exact number of followers, from the page's data. Null when the page does not carry it.
- `applicationCategory` (string | null, optional)

## FAQ

### What does "Get Product Hunt product" do?

Read a Product Hunt product page and return its profile: name, tagline, full description, the outbound website link, the categories it is listed under, its review rating and review count, how many times it has launched, its makers with their Product Hunt profiles, and any Top Product or Golden Kitty awards. Accepts either the product slug or a full Product Hunt product URL. Follower counts are returned exactly as the page displays them (Product Hunt rounds them, e.g. "18K") alongside a numeric approximation. An unknown product is reported as such rather than returned as an empty record.

### How do I automatically get Product Hunt product on producthunt.com?

Ask an AI agent connected to Reduck to run reduck/producthunt.com/get_product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/producthunt.com/get_product

### Is there a producthunt.com API to get Product Hunt product?

You do not need one. "Get Product Hunt product" drives the real producthunt.com pages in a browser, so it works whether or not producthunt.com offers an API for this.

### What information do I need to provide?

Required: product.

### What does it return?

It returns url, name, slug, makers, tagline, website, productId, categories, topProduct, description, goldenKitty, latestAward, ratingCount, ratingValue, datePublished, launchesCount, followersCount, applicationCategory.

### Do I need to be logged in to producthunt.com?

No. It only uses pages of producthunt.com that are reachable without signing in.

### Does it change anything on producthunt.com, or only read data?

It only reads. It looks things up on producthunt.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/producthunt.com/get_product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/producthunt.com/get_product

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/producthunt.com/get_product
