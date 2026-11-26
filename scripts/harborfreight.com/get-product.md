# Get a Harbor Freight product

Automatically get a Harbor Freight product on harborfreight.com. Read one Harbor Freight product by SKU or product page link: price, stock status, rating, images, brand, description and specifications.

- Site: harborfreight.com
- Address: `reduck/harborfreight.com/get-product`
- Updated: 2026-11-25 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/harborfreight.com/get-product`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/harborfreight.com/get-product
```

## Input

- `product` (string, required): The product SKU (for example 70067) or its harborfreight.com product page link.

## Output

- `id` (string, required): SKU
- `name` (string, required)
- `images` (array, required)
- `options` (array, required): The SKUs to choose from when the page groups several products (for example tool only or kit).
- `specifications` (array, required)
- `url` (string | null, optional)
- `brand` (string | null, optional)
- `price` (number | null, optional)
- `rating` (number | null, optional)
- `currency` (string | null, optional)
- `list_price` (number | null, optional)
- `description` (string | null, optional)
- `retail_only` (boolean | null, optional): Sold in stores only, not online.
- `availability` (string | null, optional): Stock status as the site states it, for example IN_STOCK or OUT_OF_STOCK.
- `review_count` (integer | null, optional)

## FAQ

### What does "Get a Harbor Freight product" do?

Read one Harbor Freight product by SKU or product page link: price, stock status, rating, images, brand, description and specifications.

### How do I automatically get a Harbor Freight product on harborfreight.com?

Ask an AI agent connected to Reduck to run reduck/harborfreight.com/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/harborfreight.com/get-product

### Is there a harborfreight.com API to get a Harbor Freight product?

You do not need one. "Get a Harbor Freight product" drives the real harborfreight.com pages in a browser, so it works whether or not harborfreight.com offers an API for this.

### What information do I need to provide?

Required: product.

### What does it return?

It returns id, url, name, brand, price, images, rating, options, currency, list_price, description, retail_only, availability, review_count, specifications.

### Do I need to be logged in to harborfreight.com?

No. It only uses pages of harborfreight.com that are reachable without signing in.

### Does it change anything on harborfreight.com, or only read data?

It only reads. It looks things up on harborfreight.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/harborfreight.com/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/harborfreight.com/get-product

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/harborfreight.com/get-product
