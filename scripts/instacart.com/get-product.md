# Get Instacart product

Automatically get Instacart product on instacart.com. Read one Instacart.com product by product id or product link, across stores: name, brand, size, category, description and detail sections, the lowest price Instacart states for it, rating out of 5, rating count and images. For each store's price, use Get Instacart product offers.

- Site: instacart.com
- Address: `reduck/instacart.com/get-product`
- Updated: 2026-11-26 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/instacart.com/get-product`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/instacart.com/get-product
```

## Input

- `product` (string, required): An Instacart product id (e.g. "16408559") or a product link containing /products/<id>, as Search Instacart store products returns.

## Output

- `url` (string, required)
- `name` (string | null, required)
- `productId` (string, required)
- `size` (string | null, optional)
- `brand` (string | null, optional)
- `rating` (number | null, optional)
- `details` (array, optional)
- `category` (string | null, optional)
- `image_urls` (array, optional)
- `description` (string | null, optional)
- `rating_count` (integer | null, optional)
- `starting_price` (number | null, optional)

## FAQ

### What does "Get Instacart product" do?

Read one Instacart.com product by product id or product link, across stores: name, brand, size, category, description and detail sections, the lowest price Instacart states for it, rating out of 5, rating count and images. For each store's price, use Get Instacart product offers.

### How do I automatically get Instacart product on instacart.com?

Ask an AI agent connected to Reduck to run reduck/instacart.com/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/instacart.com/get-product

### Is there a instacart.com API to get Instacart product?

You do not need one. "Get Instacart product" drives the real instacart.com pages in a browser, so it works whether or not instacart.com offers an API for this.

### What information do I need to provide?

Required: product.

### What does it return?

It returns url, name, size, brand, rating, details, category, productId, image_urls, description, rating_count, starting_price.

### Do I need to be logged in to instacart.com?

No. It only uses pages of instacart.com that are reachable without signing in.

### Does it change anything on instacart.com, or only read data?

It only reads. It looks things up on instacart.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/instacart.com/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/instacart.com/get-product

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/instacart.com/get-product
