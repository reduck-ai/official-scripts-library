# Get Amazon product

Automatically get Amazon product on amazon.com. Fetch a single Amazon product page by ASIN. Returns title, byline, brand, price, list_price, rating, review_count, rating_breakdown, availability, breadcrumb, image_url, feature_bullets, description, attributes, variant_asins, delivery_estimate, return_policy, and seller. The returned asin can differ from the requested one when Amazon resolves a variant. Price, feature_bullets, and attributes are often null or empty for books.

- Site: amazon.com
- Address: `reduck/amazon.com/get-product`
- Updated: 2026-08-28 (v7)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/amazon.com/get-product`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/amazon.com/get-product
```

## Input

- `asin` (string, required)
- `zipCode` (string, optional)

## Output

- `url` (string, required): Canonical product URL.
- `zip` (string, required): US ZIP the store was pinned to for this fetch.
- `asin` (string | null, required): ASIN actually displayed (differs from requested when Amazon resolves a variant).
- `brand` (string | null, required): Brand parsed from the byline.
- `price` (object | null, required): Featured-offer price as {value, currency}. Null when no single buy-now price shows (e.g. books with a binding picker). {raw,value:null} when a currency symbol couldn't be parsed.
- `title` (string | null, required)
- `byline` (string | null, required): Verbatim byline — e.g. "Visit the Anker Store", "by Author (Author)".
- `rating` (number | null, required): Average stars out of 5.
- `seller` (object | null, required): Sold-by seller {name, id}; id is null for Amazon Retail / when no seller link is shown.
- `image_url` (string | null, required): Main product image (high-res when available).
- `attributes` (object, required): Product-overview spec table; empty when not rendered.
- `breadcrumb` (array, required): Category path; empty when no wayfinding breadcrumb (e.g. Amazon devices).
- `list_price` (object | null, required): Struck-through list price as {value, currency}, when shown.
- `description` (string | null, required): Product description block, when present.
- `availability` (string | null, required): Visible availability message — "In Stock", "Only N left", or the unshippable message.
- `review_count` (integer | null, required)
- `return_policy` (string | null, required): Return policy summary, e.g. "FREE Returns".
- `variant_asins` (array, required): Sibling variant ASINs from the variation widget; empty when the product has no variations.
- `requested_asin` (string, required): ASIN passed in by the caller — the join key.
- `feature_bullets` (array, required): "About this item" bullets; empty when not rendered (e.g. books).
- `rating_breakdown` (object | null, required): Percentage of ratings per star bucket, e.g. {"5_star":"73%"}. Null when not rendered.
- `delivery_estimate` (string | null, required): Delivery date/time message, when shown.

## FAQ

### What does "Get Amazon product" do?

Fetch a single Amazon product page by ASIN. Returns title, byline, brand, price, list_price, rating, review_count, rating_breakdown, availability, breadcrumb, image_url, feature_bullets, description, attributes, variant_asins, delivery_estimate, return_policy, and seller. The returned asin can differ from the requested one when Amazon resolves a variant. Price, feature_bullets, and attributes are often null or empty for books.

### How do I automatically get Amazon product on amazon.com?

Ask an AI agent connected to Reduck to run reduck/amazon.com/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/amazon.com/get-product

### Is there a amazon.com API to get Amazon product?

You do not need one. "Get Amazon product" drives the real amazon.com pages in a browser, so it works whether or not amazon.com offers an API for this.

### What information do I need to provide?

Required: asin. Optional: zipCode.

### What does it return?

It returns url, zip, asin, brand, price, title, byline, rating, seller, image_url, attributes, breadcrumb, list_price, description, availability, review_count, return_policy, variant_asins, requested_asin, feature_bullets, rating_breakdown, delivery_estimate.

### Do I need to be logged in to amazon.com?

No. It only uses pages of amazon.com that are reachable without signing in.

### Does it change anything on amazon.com, or only read data?

It only reads. It looks things up on amazon.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/amazon.com/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/amazon.com/get-product

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/amazon.com/get-product
