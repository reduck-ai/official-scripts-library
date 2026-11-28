# Get Cultura product

Automatically get Cultura product on cultura.com. Read one cultura.com product by its link or product id.

- Site: cultura.com
- Address: `reduck/cultura.com/get-product`
- Updated: 2026-11-27 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/cultura.com/get-product`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/cultura.com/get-product
```

## Input

- `product` (string, required): A cultura.com product link (https://www.cultura.com/p-....html) or a product id from search-products.

## Output

- `id` (string, required)
- `url` (string, required)
- `ean` (string | null, optional)
- `name` (string | null, optional)
- `price` (number | null, optional)
- `rating` (number | null, optional)
- `category` (string | null, optional)
- `currency` (string, optional)
- `in_stock` (boolean, optional)
- `image_url` (string | null, optional)
- `list_price` (number | null, optional)
- `description` (string | null, optional)
- `review_count` (integer | null, optional)
- `author_or_brand` (string | null, optional)
- `marketplace_offers` (integer, optional)
- `cheapest_marketplace_price` (number | null, optional)

## FAQ

### What does "Get Cultura product" do?

Read one cultura.com product by its link or product id.

### How do I automatically get Cultura product on cultura.com?

Ask an AI agent connected to Reduck to run reduck/cultura.com/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/cultura.com/get-product

### Is there a cultura.com API to get Cultura product?

You do not need one. "Get Cultura product" drives the real cultura.com pages in a browser, so it works whether or not cultura.com offers an API for this.

### What information do I need to provide?

Required: product.

### What does it return?

It returns id, ean, url, name, price, rating, category, currency, in_stock, image_url, list_price, description, review_count, author_or_brand, marketplace_offers, cheapest_marketplace_price.

### Do I need to be logged in to cultura.com?

No. It only uses pages of cultura.com that are reachable without signing in.

### Does it change anything on cultura.com, or only read data?

It only reads. It looks things up on cultura.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/cultura.com/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/cultura.com/get-product

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/cultura.com/get-product
