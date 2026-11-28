# Get Showroomprivé product

Automatically get Showroomprivé product on showroomprive.com. Read one showroomprive.com product of an open sale by its link or id, with every size, its price and stock.

- Site: showroomprive.com
- Address: `reduck/showroomprive.com/get-product`
- Updated: 2026-11-27 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/showroomprive.com/get-product`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/showroomprive.com/get-product
```

## Input

- `product` (string, required): A showroomprive.com product link or a product id from search-products.

## Output

- `id` (string, required)
- `url` (string, required)
- `name` (string | null, optional)
- `sale` (object | null, optional)
- `brand` (string | null, optional)
- `price` (number | null, optional)
- `sizes` (array, optional)
- `colors` (array, optional)
- `seller` (string | null, optional)
- `category` (string | null, optional)
- `currency` (string, optional)
- `in_stock` (boolean, optional)
- `image_urls` (array, optional)
- `list_price` (number | null, optional)
- `discount_percent` (number | null, optional)

## FAQ

### What does "Get Showroomprivé product" do?

Read one showroomprive.com product of an open sale by its link or id, with every size, its price and stock.

### How do I automatically get Showroomprivé product on showroomprive.com?

Ask an AI agent connected to Reduck to run reduck/showroomprive.com/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/showroomprive.com/get-product

### Is there a showroomprive.com API to get Showroomprivé product?

You do not need one. "Get Showroomprivé product" drives the real showroomprive.com pages in a browser, so it works whether or not showroomprive.com offers an API for this.

### What information do I need to provide?

Required: product.

### What does it return?

It returns id, url, name, sale, brand, price, sizes, colors, seller, category, currency, in_stock, image_urls, list_price, discount_percent.

### Do I need to be logged in to showroomprive.com?

No. It only uses pages of showroomprive.com that are reachable without signing in.

### Does it change anything on showroomprive.com, or only read data?

It only reads. It looks things up on showroomprive.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/showroomprive.com/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/showroomprive.com/get-product

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/showroomprive.com/get-product
