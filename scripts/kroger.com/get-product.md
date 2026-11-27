# Get Kroger product

Automatically get Kroger product on kroger.com. Read one Kroger.com product by UPC or product link, at the store Kroger shows prices for: name, brand, size, category, description, price in US dollars, regular price when on sale, unit price text, rating, review count, image, whether food assistance benefits can pay for it, stock level, aisle, and each way to get it (pickup, delivery, in store) with whether it can be ordered and the most per order.

- Site: kroger.com
- Address: `reduck/kroger.com/get-product`
- Updated: 2026-11-26 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/kroger.com/get-product`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/kroger.com/get-product
```

## Input

- `product` (string, required): A 13-digit Kroger UPC (e.g. "0001111041600") or a product link ending in it, as returned by Search Kroger products.

## Output

- `upc` (string, required)
- `url` (string, required)
- `name` (string | null, required)
- `size` (string | null, optional)
- `aisle` (string | null, optional)
- `brand` (string | null, optional)
- `price` (number | null, optional)
- `rating` (number | null, optional)
- `category` (string | null, optional)
- `image_url` (string | null, optional)
- `description` (string | null, optional)
- `fulfillment` (array, optional)
- `location_id` (string | null, optional)
- `stock_level` (string | null, optional)
- `review_count` (integer | null, optional)
- `regular_price` (number | null, optional)
- `snap_eligible` (boolean | null, optional)
- `unit_price_text` (string | null, optional)

## FAQ

### What does "Get Kroger product" do?

Read one Kroger.com product by UPC or product link, at the store Kroger shows prices for: name, brand, size, category, description, price in US dollars, regular price when on sale, unit price text, rating, review count, image, whether food assistance benefits can pay for it, stock level, aisle, and each way to get it (pickup, delivery, in store) with whether it can be ordered and the most per order.

### How do I automatically get Kroger product on kroger.com?

Ask an AI agent connected to Reduck to run reduck/kroger.com/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/kroger.com/get-product

### Is there a kroger.com API to get Kroger product?

You do not need one. "Get Kroger product" drives the real kroger.com pages in a browser, so it works whether or not kroger.com offers an API for this.

### What information do I need to provide?

Required: product.

### What does it return?

It returns upc, url, name, size, aisle, brand, price, rating, category, image_url, description, fulfillment, location_id, stock_level, review_count, regular_price, snap_eligible, unit_price_text.

### Do I need to be logged in to kroger.com?

No. It only uses pages of kroger.com that are reachable without signing in.

### Does it change anything on kroger.com, or only read data?

It only reads. It looks things up on kroger.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/kroger.com/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/kroger.com/get-product

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/kroger.com/get-product
