# Get Kohl's product

Automatically get Kohl's product on kohls.com. Read one Kohls.com product by its link: name, brand, stock status, current, regular and offer prices in US dollars, rating, review count, return policy, description, image, the preselected SKU, and every SKU with its color, size, availability, the most that can be ordered and its prices. Takes the link Search Kohl's products returns.

- Site: kohls.com
- Address: `reduck/kohls.com/get-product`
- Updated: 2026-11-27 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/kohls.com/get-product`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/kohls.com/get-product
```

## Input

- `url` (string, required): The product's link as Search Kohl's products returns it (https://www.kohls.com/product/prd-<id>/<name>.jsp).

## Output

- `id` (string, required)
- `url` (string, required)
- `name` (string | null, required)
- `skus` (array, required)
- `brand` (string | null, optional)
- `price` (number | null, optional): Lowest current price in US dollars (sale, or regular when not on sale).
- `rating` (number | null, optional)
- `status` (string | null, optional): Product status as Kohl's states it, e.g. In Stock.
- `image_url` (string | null, optional)
- `your_price` (number | null, optional): The lower price Kohl's shows after its automatic offer, when it shows one.
- `review_count` (integer | null, optional)
- `selected_sku` (string | null, optional)
- `regular_price` (number | null, optional)
- `return_policy` (string | null, optional)
- `description_html` (string | null, optional)

## FAQ

### What does "Get Kohl's product" do?

Read one Kohls.com product by its link: name, brand, stock status, current, regular and offer prices in US dollars, rating, review count, return policy, description, image, the preselected SKU, and every SKU with its color, size, availability, the most that can be ordered and its prices. Takes the link Search Kohl's products returns.

### How do I automatically get Kohl's product on kohls.com?

Ask an AI agent connected to Reduck to run reduck/kohls.com/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/kohls.com/get-product

### Is there a kohls.com API to get Kohl's product?

You do not need one. "Get Kohl's product" drives the real kohls.com pages in a browser, so it works whether or not kohls.com offers an API for this.

### What information do I need to provide?

Required: url.

### What does it return?

It returns id, url, name, skus, brand, price, rating, status, image_url, your_price, review_count, selected_sku, regular_price, return_policy, description_html.

### Do I need to be logged in to kohls.com?

No. It only uses pages of kohls.com that are reachable without signing in.

### Does it change anything on kohls.com, or only read data?

It only reads. It looks things up on kohls.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/kohls.com/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/kohls.com/get-product

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/kohls.com/get-product
