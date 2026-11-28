# Get Kaufland product

Automatically get Kaufland product on kaufland.de. Read one kaufland.de product by its link: name, brand, barcode (gtin), category, description, image, the buy-box price in euros with its seller, shipping fee, return days and stock state, rating, review count, and the product's variants with their ids and attributes. Takes the link Search Kaufland products returns.

- Site: kaufland.de
- Address: `reduck/kaufland.de/get-product`
- Updated: 2026-11-27 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/kaufland.de/get-product`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/kaufland.de/get-product
```

## Input

- `url` (string, required): The product's link as Search Kaufland products returns it (https://www.kaufland.de/product/<id>/).

## Output

- `id` (string, required)
- `url` (string, required)
- `name` (string, required)
- `variants` (array, required)
- `gtin` (string | null, optional)
- `brand` (string | null, optional)
- `price` (number | null, optional)
- `rating` (number | null, optional)
- `seller` (string | null, optional)
- `category` (string | null, optional)
- `currency` (string, optional)
- `image_url` (string | null, optional)
- `description` (string | null, optional)
- `return_days` (integer | null, optional)
- `availability` (string | null, optional)
- `review_count` (integer | null, optional)
- `shipping_fee` (number | null, optional)

## FAQ

### What does "Get Kaufland product" do?

Read one kaufland.de product by its link: name, brand, barcode (gtin), category, description, image, the buy-box price in euros with its seller, shipping fee, return days and stock state, rating, review count, and the product's variants with their ids and attributes. Takes the link Search Kaufland products returns.

### How do I automatically get Kaufland product on kaufland.de?

Ask an AI agent connected to Reduck to run reduck/kaufland.de/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/kaufland.de/get-product

### Is there a kaufland.de API to get Kaufland product?

You do not need one. "Get Kaufland product" drives the real kaufland.de pages in a browser, so it works whether or not kaufland.de offers an API for this.

### What information do I need to provide?

Required: url.

### What does it return?

It returns id, url, gtin, name, brand, price, rating, seller, category, currency, variants, image_url, description, return_days, availability, review_count, shipping_fee.

### Do I need to be logged in to kaufland.de?

No. It only uses pages of kaufland.de that are reachable without signing in.

### Does it change anything on kaufland.de, or only read data?

It only reads. It looks things up on kaufland.de and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/kaufland.de/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/kaufland.de/get-product

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/kaufland.de/get-product
