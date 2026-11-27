# Get L.L.Bean product

Automatically get L.L.Bean product on llbean.com. Get one L.L.Bean (llbean.com, US) product by its id or link: name, price range in USD, rating, images, its options (color, size and others), its details, and every variant with its color, size, price and stock status. An id that L.L.Bean does not have gives an error that says so.

- Site: llbean.com
- Address: `reduck/llbean.com/get-product`
- Updated: 2026-11-26 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/llbean.com/get-product`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/llbean.com/get-product
```

## Input

- `product` (string, required): Product id (the number after /llb/shop/ in a product link, for example 128942), as Search L.L.Bean products gives it, or the product link.

## Output

- `id` (string, required)
- `url` (string, required)
- `name` (string, required)
- `variants` (array, required)
- `images` (array, optional)
- `rating` (number | null, optional)
- `details` (array, optional)
- `options` (array, optional)
- `currency` (string, optional)
- `image_url` (string | null, optional)
- `price_low` (number | null, optional): Lowest price of the variants, in USD.
- `price_high` (number | null, optional)
- `review_count` (integer | null, optional)

## FAQ

### What does "Get L.L.Bean product" do?

Get one L.L.Bean (llbean.com, US) product by its id or link: name, price range in USD, rating, images, its options (color, size and others), its details, and every variant with its color, size, price and stock status. An id that L.L.Bean does not have gives an error that says so.

### How do I automatically get L.L.Bean product on llbean.com?

Ask an AI agent connected to Reduck to run reduck/llbean.com/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/llbean.com/get-product

### Is there a llbean.com API to get L.L.Bean product?

You do not need one. "Get L.L.Bean product" drives the real llbean.com pages in a browser, so it works whether or not llbean.com offers an API for this.

### What information do I need to provide?

Required: product.

### What does it return?

It returns id, url, name, images, rating, details, options, currency, variants, image_url, price_low, price_high, review_count.

### Do I need to be logged in to llbean.com?

No. It only uses pages of llbean.com that are reachable without signing in.

### Does it change anything on llbean.com, or only read data?

It only reads. It looks things up on llbean.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/llbean.com/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/llbean.com/get-product

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/llbean.com/get-product
