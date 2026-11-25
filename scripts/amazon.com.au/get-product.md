# Get Amazon.com.au product

Automatically get Amazon.com.au product on amazon.com.au. Fetch one Amazon.com.au product page by ASIN: title, byline, brand, price in Australian dollars, list price, rating, review count, rating breakdown, availability, breadcrumb, image, feature bullets, description, attributes, variants, deal, badges, delivery estimate, return policy and seller. deal is the deal the page shows: its id, its label as Amazon writes it (for example "Black Friday Deal" or "Limited time deal") and its end time. badges are the other badges next to the title, for example Amazon's Choice. Prices and availability are pinned to an Australian postcode. The returned asin can differ from the requested one when Amazon resolves a variant.

- Site: amazon.com.au
- Address: `reduck/amazon.com.au/get-product`
- Updated: 2026-11-24 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/amazon.com.au/get-product`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/amazon.com.au/get-product
```

## Input

- `asin` (string, required): 10-character Amazon ASIN, as in /dp/<ASIN>.
- `zipCode` (string, optional): Australian postcode used to pin the store location (prices, availability).

## Output

- `url` (string, required): Canonical URL the page declares.
- `zip` (string, required): Australian postcode the store was pinned to for this fetch.
- `asin` (string | null, required): ASIN displayed (differs from the requested one when Amazon resolves a variant).
- `deal` (object | null, required): The deal that the page shows for this product. Null when there is no deal. A deal can apply to one variant only: then only the ASIN of that variant shows it.
- `price` (object | null, required): Featured-offer price as {value, currency}, in AUD. Null when no buy-now price shows.
- `title` (string | null, required)
- `badges` (array, required): Badges next to the title, other than the deal. Empty when there are none.
- `seller` (object | null, required): Sold-by seller {name, id}; id is null for Amazon Retail or when no seller link is shown.
- `variant_asins` (array, required)
- `requested_asin` (string, required)
- `brand` (string | null, optional)
- `byline` (string | null, optional)
- `rating` (number | null, optional): Average stars out of 5.
- `image_url` (string | null, optional)
- `attributes` (object, optional)
- `breadcrumb` (array, optional)
- `list_price` (object | null, optional): Struck-through list price as {value, currency}, when shown.
- `description` (string | null, optional)
- `availability` (string | null, optional)
- `review_count` (integer | null, optional)
- `return_policy` (string | null, optional)
- `feature_bullets` (array, optional)
- `rating_breakdown` (object | null, optional)
- `delivery_estimate` (string | null, optional)

## FAQ

### What does "Get Amazon.com.au product" do?

Fetch one Amazon.com.au product page by ASIN: title, byline, brand, price in Australian dollars, list price, rating, review count, rating breakdown, availability, breadcrumb, image, feature bullets, description, attributes, variants, deal, badges, delivery estimate, return policy and seller. deal is the deal the page shows: its id, its label as Amazon writes it (for example "Black Friday Deal" or "Limited time deal") and its end time. badges are the other badges next to the title, for example Amazon's Choice. Prices and availability are pinned to an Australian postcode. The returned asin can differ from the requested one when Amazon resolves a variant.

### How do I automatically get Amazon.com.au product on amazon.com.au?

Ask an AI agent connected to Reduck to run reduck/amazon.com.au/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/amazon.com.au/get-product

### Is there a amazon.com.au API to get Amazon.com.au product?

You do not need one. "Get Amazon.com.au product" drives the real amazon.com.au pages in a browser, so it works whether or not amazon.com.au offers an API for this.

### What information do I need to provide?

Required: asin. Optional: zipCode.

### What does it return?

It returns url, zip, asin, deal, brand, price, title, badges, byline, rating, seller, image_url, attributes, breadcrumb, list_price, description, availability, review_count, return_policy, variant_asins, requested_asin, feature_bullets, rating_breakdown, delivery_estimate.

### Do I need to be logged in to amazon.com.au?

No. It only uses pages of amazon.com.au that are reachable without signing in.

### Does it change anything on amazon.com.au, or only read data?

It only reads. It looks things up on amazon.com.au and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/amazon.com.au/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/amazon.com.au/get-product

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/amazon.com.au/get-product
