# Get Intersport product

Automatically get Intersport product on intersport.fr. Read one intersport.fr product colour by its link or code, with its sizes and their stock.

- Site: intersport.fr
- Address: `reduck/intersport.fr/get-product`
- Updated: 2026-11-27 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/intersport.fr/get-product`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/intersport.fr/get-product
```

## Input

- `product` (string, required): An intersport.fr product link (https://www.intersport.fr/...-p-<code>/) or a code from search-products.

## Output

- `id` (string, required)
- `url` (string, required)
- `name` (string | null, required)
- `price` (number | null, required)
- `sizes` (array, required)
- `currency` (string, required)
- `brand` (string | null, optional)
- `color` (string | null, optional)
- `gender` (string | null, optional)
- `category` (string | null, optional)
- `in_stock` (boolean, optional)
- `promotion` (string | null, optional)
- `image_urls` (array, optional)
- `list_price` (number | null, optional)
- `description` (string | null, optional)
- `other_colors` (array, optional)
- `discount_percent` (number | null, optional)

## FAQ

### What does "Get Intersport product" do?

Read one intersport.fr product colour by its link or code, with its sizes and their stock.

### How do I automatically get Intersport product on intersport.fr?

Ask an AI agent connected to Reduck to run reduck/intersport.fr/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/intersport.fr/get-product

### Is there a intersport.fr API to get Intersport product?

You do not need one. "Get Intersport product" drives the real intersport.fr pages in a browser, so it works whether or not intersport.fr offers an API for this.

### What information do I need to provide?

Required: product.

### What does it return?

It returns id, url, name, brand, color, price, sizes, gender, category, currency, in_stock, promotion, image_urls, list_price, description, other_colors, discount_percent.

### Do I need to be logged in to intersport.fr?

No. It only uses pages of intersport.fr that are reachable without signing in.

### Does it change anything on intersport.fr, or only read data?

It only reads. It looks things up on intersport.fr and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/intersport.fr/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/intersport.fr/get-product

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/intersport.fr/get-product
