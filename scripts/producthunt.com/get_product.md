# Get Product Hunt product

Automatically get Product Hunt product on producthunt.com. Read a Product Hunt product page and return its profile: name, tagline, full description, the outbound website link, the categories it is listed under, its review rating and review count, how many times it has launched, its makers with their Product Hunt profiles, and any Top Product or Golden Kitty awards. Accepts either the product slug or a full Product Hunt product URL. Follower counts are returned exactly as the page displays them (Product Hunt rounds them, e.g. "18K") alongside a numeric approximation. An unknown product is reported as such rather than returned as an empty record.

- Site: producthunt.com
- Address: `reduck/producthunt.com/get_product`
- Updated: 2026-09-08 (v4)
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
- `slug` (string, required): The product's slug on Product Hunt — the join key for its launches and reviews pages.
- `makers` (array, required): People credited on the product, with their Product Hunt profiles. Empty when none are credited.
- `categories` (array, required): Categories this product is listed under. Empty for products that have not been categorised.
- `tagline` (string | null, optional): One-line pitch shown under the product name.
- `website` (string | null, optional): The product's own site, as linked from the page. Null when no site is linked.
- `productId` (string | null, optional): Product Hunt's own numeric product identifier, when the page exposes it.
- `topProduct` (boolean, optional): Whether the page shows a Top Product badge.
- `description` (string | null, optional): Longer product description. Null when the product has not published one.
- `goldenKitty` (boolean, optional): Whether the page shows a Golden Kitty award badge.
- `latestAward` (string | null, optional): Text of the most recent award callout, when one is shown.
- `ratingCount` (number | null, optional): Number of reviews behind the average. Null when the product has no reviews yet.
- `ratingValue` (number | null, optional): Average review score out of 5. Null when the product has no reviews yet.
- `datePublished` (string | null, optional): ISO timestamp of when the product profile was first published.
- `launchesCount` (number | null, optional): How many times this product has launched on Product Hunt.
- `followersApprox` (number | null, optional): The rounded display value parsed to a number. Approximate by construction — Product Hunt does not publish an exact figure here.
- `followersDisplay` (string | null, optional): Follower count exactly as shown on the page, which Product Hunt rounds (e.g. "18K").
- `applicationCategory` (string | null, optional): The single category Product Hunt files the product under in its structured data. Can disagree with the visible category list — it is reported as the site states it, not corrected.

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

It returns url, name, slug, makers, tagline, website, productId, categories, topProduct, description, goldenKitty, latestAward, ratingCount, ratingValue, datePublished, launchesCount, followersApprox, followersDisplay, applicationCategory.

### Do I need to be logged in to producthunt.com?

No. It only uses pages of producthunt.com that are reachable without signing in.

### Does it change anything on producthunt.com, or only read data?

It only reads. It looks things up on producthunt.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/producthunt.com/get_product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/producthunt.com/get_product

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/producthunt.com/get_product
