# Get AliExpress product

Automatically get AliExpress product on aliexpress.com. Read an AliExpress product page by item id: title, description, price and currency, availability, rating, review count, images, store, and the raw sold-count text. Anonymous, read-only. Pairs with aliexpress.com/search_products, whose result `id` is this script's `itemId`. Price, currency and soldText reflect whatever locale/currency AliExpress geo-resolves the session to, so they legitimately vary by caller.

- Site: aliexpress.com
- Address: `reduck/aliexpress.com/get_product`
- Updated: 2026-09-18 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/aliexpress.com/get_product`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/aliexpress.com/get_product
```

## Input

- `itemId` (string | number, required): AliExpress numeric item id, e.g. 1005012250100905 — the `id` field returned by aliexpress.com/search_products, or the digits in an /item/<id>.html URL.

## Output

- `url` (string, required): The product URL landed on, after AliExpress's geo redirect (e.g. fr.aliexpress.com).
- `title` (string | null, required)
- `images` (array, required): Product image URLs from the page's structured data. AliExpress repeats the same URL across entries for some items, so duplicates are de-duplicated here.
- `itemId` (string, required): The item id as requested, echoed for joining.
- `currency` (string | null, required): ISO currency code of priceText, geo-resolved by AliExpress (e.g. EUR, USD).
- `priceText` (string | null, required): Price as a decimal string exactly as the page's structured data states it (e.g. "1.91"). Kept as a string to avoid float rounding; pair with `currency`.
- `rating` (number | null, optional): Average rating out of 5. Null is legitimate: a product with no ratings yet publishes no aggregateRating.
- `storeId` (string | null, optional): Numeric store id from the seller's /store/<id> link — locale-proof join key for the seller.
- `soldText` (string | null, optional): Raw sold-count text as rendered (e.g. "+ 2 000 vendus"). Not parsed: AliExpress localises both the wording and the thousand separators, so any parse would be lossy. Null when the page shows no sold count.
- `storeUrl` (string | null, optional)
- `storeName` (string | null, optional)
- `description` (string | null, optional)
- `reviewCount` (integer | null, optional): Number of reviews behind `rating`. Null when the product has no ratings.
- `availability` (string | null, optional): Schema.org availability URL, e.g. https://schema.org/InStock.
- `canonicalItemId` (string | null, optional): The item id in the page's own canonical link. Normally equal to itemId; if AliExpress resolved the request to a different item, the two disagree and this is the one actually described.

## FAQ

### What does "Get AliExpress product" do?

Read an AliExpress product page by item id: title, description, price and currency, availability, rating, review count, images, store, and the raw sold-count text. Anonymous, read-only. Pairs with aliexpress.com/search_products, whose result `id` is this script's `itemId`. Price, currency and soldText reflect whatever locale/currency AliExpress geo-resolves the session to, so they legitimately vary by caller.

### How do I automatically get AliExpress product on aliexpress.com?

Ask an AI agent connected to Reduck to run reduck/aliexpress.com/get_product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/aliexpress.com/get_product

### Is there a aliexpress.com API to get AliExpress product?

You do not need one. "Get AliExpress product" drives the real aliexpress.com pages in a browser, so it works whether or not aliexpress.com offers an API for this.

### What information do I need to provide?

Required: itemId.

### What does it return?

It returns url, title, images, itemId, rating, storeId, currency, soldText, storeUrl, priceText, storeName, description, reviewCount, availability, canonicalItemId.

### Do I need to be logged in to aliexpress.com?

No. It only uses pages of aliexpress.com that are reachable without signing in.

### Does it change anything on aliexpress.com, or only read data?

It only reads. It looks things up on aliexpress.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/aliexpress.com/get_product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/aliexpress.com/get_product

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/aliexpress.com/get_product
