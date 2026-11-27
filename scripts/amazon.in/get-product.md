# Get Amazon.in product

Automatically get Amazon.in product on amazon.in. Fetch a single Amazon.in product page by ASIN. Returns title, byline, brand, price and its currency, list_price, rating, review_count, rating_breakdown, availability, breadcrumb, image_url, feature_bullets, description, attributes, variant_asins, deal, badges, delivery_estimate, return_policy, and seller. deal is the deal the page shows: its id, its label as Amazon writes it and its end time. badges are the other badges next to the title, for example Amazon's Choice. The returned asin can differ from the requested one when Amazon resolves a variant. For books, brand is null and feature_bullets and attributes are usually empty.

- Site: amazon.in
- Address: `reduck/amazon.in/get-product`
- Updated: 2026-11-26 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/amazon.in/get-product`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/amazon.in/get-product
```

## Input

- `asin` (string, required)
- `zipCode` (string, optional)

## Output

- `url` (string, required): Canonical URL the page declares. Usually /dp/<asin>.
- `zip` (string, required): Indian PIN code the store was pinned to for this fetch.
- `asin` (string | null, required): ASIN actually displayed (differs from requested when Amazon resolves a variant).
- `deal` (object | null, required): The deal that the page shows for this product. Null when there is no deal.
- `brand` (string | null, required): Brand parsed from the byline. Null for books.
- `price` (object | null, required): Featured-offer price as {value, currency}. Null when no buy-now price shows.
- `title` (string | null, required)
- `badges` (array, required): Badges next to the title, other than the deal.
- `byline` (string | null, required): Verbatim byline.
- `rating` (number | null, required): Average stars out of 5.
- `seller` (object | null, required): Sold-by seller {name, id}; id is null when no seller link is shown.
- `image_url` (string | null, required)
- `attributes` (object, required): Product-overview spec table; empty when not rendered.
- `breadcrumb` (array, required)
- `list_price` (object | null, required): Struck-through list price as {value, currency}, when shown.
- `description` (string | null, required)
- `availability` (string | null, required)
- `review_count` (integer | null, required)
- `return_policy` (string | null, required)
- `variant_asins` (array, required)
- `requested_asin` (string, required): ASIN passed in by the caller.
- `feature_bullets` (array, required)
- `rating_breakdown` (object | null, required)
- `delivery_estimate` (string | null, required)

## FAQ

### What does "Get Amazon.in product" do?

Fetch a single Amazon.in product page by ASIN. Returns title, byline, brand, price and its currency, list_price, rating, review_count, rating_breakdown, availability, breadcrumb, image_url, feature_bullets, description, attributes, variant_asins, deal, badges, delivery_estimate, return_policy, and seller. deal is the deal the page shows: its id, its label as Amazon writes it and its end time. badges are the other badges next to the title, for example Amazon's Choice. The returned asin can differ from the requested one when Amazon resolves a variant. For books, brand is null and feature_bullets and attributes are usually empty.

### How do I automatically get Amazon.in product on amazon.in?

Ask an AI agent connected to Reduck to run reduck/amazon.in/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/amazon.in/get-product

### Is there a amazon.in API to get Amazon.in product?

You do not need one. "Get Amazon.in product" drives the real amazon.in pages in a browser, so it works whether or not amazon.in offers an API for this.

### What information do I need to provide?

Required: asin. Optional: zipCode.

### What does it return?

It returns url, zip, asin, deal, brand, price, title, badges, byline, rating, seller, image_url, attributes, breadcrumb, list_price, description, availability, review_count, return_policy, variant_asins, requested_asin, feature_bullets, rating_breakdown, delivery_estimate.

### Do I need to be logged in to amazon.in?

No. It only uses pages of amazon.in that are reachable without signing in.

### Does it change anything on amazon.in, or only read data?

It only reads. It looks things up on amazon.in and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/amazon.in/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/amazon.in/get-product

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/amazon.in/get-product
