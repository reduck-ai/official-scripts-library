# Get lululemon product

Automatically get lululemon product on lululemon.com. Read one shop.lululemon.com product by its link or id, with colours, sizes and stock.

- Site: lululemon.com
- Address: `reduck/lululemon.com/get-product`
- Updated: 2026-11-27 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/lululemon.com/get-product`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/lululemon.com/get-product
```

## Input

- `product` (string, required): A shop.lululemon.com product link (https://shop.lululemon.com/p/...) or a product id from search-products.

## Output

- `id` (string, required)
- `url` (string, required)
- `name` (string | null, optional)
- `price` (number | null, optional): Lowest current price across colours and sizes
- `sizes` (array, optional)
- `colors` (array, optional)
- `fabric` (string | null, optional)
- `gender` (string | null, optional)
- `category` (string | null, optional)
- `currency` (string, optional)
- `features` (array, optional)
- `in_stock` (boolean, optional)
- `variants` (array, optional): Every colour and size, with its sku
- `max_price` (number | null, optional)
- `image_urls` (array, optional)
- `description` (string | null, optional)

## FAQ

### What does "Get lululemon product" do?

Read one shop.lululemon.com product by its link or id, with colours, sizes and stock.

### How do I automatically get lululemon product on lululemon.com?

Ask an AI agent connected to Reduck to run reduck/lululemon.com/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/lululemon.com/get-product

### Is there a lululemon.com API to get lululemon product?

You do not need one. "Get lululemon product" drives the real lululemon.com pages in a browser, so it works whether or not lululemon.com offers an API for this.

### What information do I need to provide?

Required: product.

### What does it return?

It returns id, url, name, price, sizes, colors, fabric, gender, category, currency, features, in_stock, variants, max_price, image_urls, description.

### Do I need to be logged in to lululemon.com?

No. It only uses pages of lululemon.com that are reachable without signing in.

### Does it change anything on lululemon.com, or only read data?

It only reads. It looks things up on lululemon.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/lululemon.com/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/lululemon.com/get-product

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/lululemon.com/get-product
