# Get Amazon.com.mx product

Automatically get Amazon.com.mx product on amazon.com.mx. Fetch one Amazon.com.mx product page by ASIN: title, byline, brand, price in Mexican pesos, list price, rating, review count, rating breakdown, availability, breadcrumb, image, feature bullets, description, attributes, variants, deal, badges, delivery estimate, return policy and seller. deal is the deal the page shows: its id, its label as Amazon writes it and its end time. badges are the other badges next to the title. The returned asin can differ from the requested one when Amazon resolves a variant.

- Site: amazon.com.mx
- Address: `reduck/amazon.com.mx/get-product`
- Updated: 2026-11-24 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/amazon.com.mx/get-product`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/amazon.com.mx/get-product
```

## Input

- `asin` (string, required): 10-character Amazon ASIN, as in /dp/<ASIN>.
- `zipCode` (string, optional): Mexican postcode used to pin the store location.

## Output

- `url` (string, required)
- `zip` (string, required)
- `asin` (string | null, required)
- `deal` (object | null, required)
- `price` (object | null, required)
- `title` (string | null, required)
- `badges` (array, required)
- `seller` (object | null, required)
- `variant_asins` (array, required)
- `requested_asin` (string, required)
- `brand` (string | null, optional)
- `byline` (string | null, optional)
- `rating` (number | null, optional)
- `image_url` (string | null, optional)
- `attributes` (object, optional)
- `breadcrumb` (array, optional)
- `list_price` (object | null, optional)
- `description` (string | null, optional)
- `availability` (string | null, optional)
- `review_count` (integer | null, optional)
- `return_policy` (string | null, optional)
- `feature_bullets` (array, optional)
- `rating_breakdown` (object | null, optional)
- `delivery_estimate` (string | null, optional)

## FAQ

### What does "Get Amazon.com.mx product" do?

Fetch one Amazon.com.mx product page by ASIN: title, byline, brand, price in Mexican pesos, list price, rating, review count, rating breakdown, availability, breadcrumb, image, feature bullets, description, attributes, variants, deal, badges, delivery estimate, return policy and seller. deal is the deal the page shows: its id, its label as Amazon writes it and its end time. badges are the other badges next to the title. The returned asin can differ from the requested one when Amazon resolves a variant.

### How do I automatically get Amazon.com.mx product on amazon.com.mx?

Ask an AI agent connected to Reduck to run reduck/amazon.com.mx/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/amazon.com.mx/get-product

### Is there a amazon.com.mx API to get Amazon.com.mx product?

You do not need one. "Get Amazon.com.mx product" drives the real amazon.com.mx pages in a browser, so it works whether or not amazon.com.mx offers an API for this.

### What information do I need to provide?

Required: asin. Optional: zipCode.

### What does it return?

It returns url, zip, asin, deal, brand, price, title, badges, byline, rating, seller, image_url, attributes, breadcrumb, list_price, description, availability, review_count, return_policy, variant_asins, requested_asin, feature_bullets, rating_breakdown, delivery_estimate.

### Do I need to be logged in to amazon.com.mx?

No. It only uses pages of amazon.com.mx that are reachable without signing in.

### Does it change anything on amazon.com.mx, or only read data?

It only reads. It looks things up on amazon.com.mx and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/amazon.com.mx/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/amazon.com.mx/get-product

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/amazon.com.mx/get-product
