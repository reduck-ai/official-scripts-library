# Get John Lewis product

Automatically get John Lewis product on johnlewis.com. Read one product of the John Lewis UK store (johnlewis.com) by its product number or link. Returns the product number, link, title, brand, lowest and highest price in pounds sterling, rating, review count, description, category path, specifications, offer labels, the delivery and collection options with their prices, and every variant (colour or size) with its sku id, price, earlier price when reduced, availability, link and barcode. Pass a variant's sku id to Add John Lewis product to basket. An unknown product number, and a link that John Lewis answers with its "page not found" page, fail with an error that says so.

- Site: johnlewis.com
- Address: `reduck/johnlewis.com/get-product`
- Updated: 2026-11-26 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/johnlewis.com/get-product`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/johnlewis.com/get-product
```

## Input

- `product` (string, required): John Lewis product number (product_id of Search John Lewis products, for example "112182670") or product link (https://www.johnlewis.com/<name>/p<number>).

## Output

- `url` (string, required)
- `brand` (string | null, required)
- `price` (number | null, required): Lowest price of the variants, in pounds sterling.
- `title` (string | null, required)
- `images` (array, required)
- `rating` (number | null, required)
- `currency` (string, required)
- `messages` (array, required)
- `variants` (array, required)
- `price_max` (number | null, required): Highest price of the variants, in pounds sterling.
- `categories` (array, required)
- `product_id` (string, required)
- `description` (string | null, required): Product description as plain text.
- `review_count` (integer | null, required)
- `specifications` (array, required)
- `delivery_options` (array, required)

## FAQ

### What does "Get John Lewis product" do?

Read one product of the John Lewis UK store (johnlewis.com) by its product number or link. Returns the product number, link, title, brand, lowest and highest price in pounds sterling, rating, review count, description, category path, specifications, offer labels, the delivery and collection options with their prices, and every variant (colour or size) with its sku id, price, earlier price when reduced, availability, link and barcode. Pass a variant's sku id to Add John Lewis product to basket. An unknown product number, and a link that John Lewis answers with its "page not found" page, fail with an error that says so.

### How do I automatically get John Lewis product on johnlewis.com?

Ask an AI agent connected to Reduck to run reduck/johnlewis.com/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/johnlewis.com/get-product

### Is there a johnlewis.com API to get John Lewis product?

You do not need one. "Get John Lewis product" drives the real johnlewis.com pages in a browser, so it works whether or not johnlewis.com offers an API for this.

### What information do I need to provide?

Required: product.

### What does it return?

It returns url, brand, price, title, images, rating, currency, messages, variants, price_max, categories, product_id, description, review_count, specifications, delivery_options.

### Do I need to be logged in to johnlewis.com?

No. It only uses pages of johnlewis.com that are reachable without signing in.

### Does it change anything on johnlewis.com, or only read data?

It only reads. It looks things up on johnlewis.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/johnlewis.com/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/johnlewis.com/get-product

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/johnlewis.com/get-product
