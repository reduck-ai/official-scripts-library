# Get Container Store product

Automatically get Container Store product on containerstore.com. Get one product of The Container Store (containerstore.com, US) by its id or link: name, brand, category, price and list price, description, images, its options (color, size and others) and every variant with its options, price in USD, dimensions and shipping status. An id that the site does not have gives an error that says so.

- Site: containerstore.com
- Address: `reduck/containerstore.com/get-product`
- Updated: 2026-11-26 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/containerstore.com/get-product`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/containerstore.com/get-product
```

## Input

- `product` (string, required): Product id (the productId in a product link, for example 10022942), as Search Container Store products gives it, or the product link.

## Output

- `id` (string, required)
- `url` (string, required)
- `name` (string, required)
- `variants` (array, required)
- `brand` (string | null, optional)
- `images` (array, optional)
- `on_sale` (boolean | null, optional)
- `options` (array, optional)
- `category` (string | null, optional)
- `price_text` (string | null, optional)
- `description` (string | null, optional)
- `list_price_text` (string | null, optional)

## FAQ

### What does "Get Container Store product" do?

Get one product of The Container Store (containerstore.com, US) by its id or link: name, brand, category, price and list price, description, images, its options (color, size and others) and every variant with its options, price in USD, dimensions and shipping status. An id that the site does not have gives an error that says so.

### How do I automatically get Container Store product on containerstore.com?

Ask an AI agent connected to Reduck to run reduck/containerstore.com/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/containerstore.com/get-product

### Is there a containerstore.com API to get Container Store product?

You do not need one. "Get Container Store product" drives the real containerstore.com pages in a browser, so it works whether or not containerstore.com offers an API for this.

### What information do I need to provide?

Required: product.

### What does it return?

It returns id, url, name, brand, images, on_sale, options, category, variants, price_text, description, list_price_text.

### Do I need to be logged in to containerstore.com?

No. It only uses pages of containerstore.com that are reachable without signing in.

### Does it change anything on containerstore.com, or only read data?

It only reads. It looks things up on containerstore.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/containerstore.com/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/containerstore.com/get-product

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/containerstore.com/get-product
