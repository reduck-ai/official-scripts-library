# Get Sephora France product

Automatically get Sephora France product on sephora.fr. Read one sephora.fr product by its link: name, brand, price, former price and discount in euros, rating, review count, stock level, whether it can be ordered, images, category path, and every shade or size with its sku, price and availability. Takes the link Search Sephora France products returns.

- Site: sephora.fr
- Address: `reduck/sephora.fr/get-product`
- Updated: 2026-11-27 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/sephora.fr/get-product`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/sephora.fr/get-product
```

## Input

- `url` (string, required): The product's link as Search Sephora France products returns it (https://www.sephora.fr/p/....html).

## Output

- `id` (string, required): The product's master id.
- `url` (string, required)
- `name` (string, required)
- `variants` (array, required)
- `orderable` (boolean, required)
- `sku` (string | null, optional): The sku the page opened on.
- `brand` (string | null, optional)
- `price` (number | null, optional)
- `images` (array, optional)
- `rating` (number | null, optional)
- `category` (array, optional)
- `currency` (string, optional)
- `stock_level` (integer | null, optional)
- `review_count` (integer | null, optional)
- `original_price` (number | null, optional)
- `discount_percent` (number | null, optional)

## FAQ

### What does "Get Sephora France product" do?

Read one sephora.fr product by its link: name, brand, price, former price and discount in euros, rating, review count, stock level, whether it can be ordered, images, category path, and every shade or size with its sku, price and availability. Takes the link Search Sephora France products returns.

### How do I automatically get Sephora France product on sephora.fr?

Ask an AI agent connected to Reduck to run reduck/sephora.fr/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/sephora.fr/get-product

### Is there a sephora.fr API to get Sephora France product?

You do not need one. "Get Sephora France product" drives the real sephora.fr pages in a browser, so it works whether or not sephora.fr offers an API for this.

### What information do I need to provide?

Required: url.

### What does it return?

It returns id, sku, url, name, brand, price, images, rating, category, currency, variants, orderable, stock_level, review_count, original_price, discount_percent.

### Do I need to be logged in to sephora.fr?

No. It only uses pages of sephora.fr that are reachable without signing in.

### Does it change anything on sephora.fr, or only read data?

It only reads. It looks things up on sephora.fr and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/sephora.fr/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/sephora.fr/get-product

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/sephora.fr/get-product
