# Get Macy's product

Automatically get Macy's product on macys.com. Read one Macys.com product by id or link: name, brand, description, bullet points, price and regular price in US dollars, price text and deal label, when the price ends, rating, review count, the most per order, image, and every variant (UPC id and number, color, size, in stock, price).

- Site: macys.com
- Address: `reduck/macys.com/get-product`
- Updated: 2026-11-26 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/macys.com/get-product`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/macys.com/get-product
```

## Input

- `product` (string, required): A Macy's product id (e.g. "17539687") or a product link with ?ID=, as returned by Search Macy's products.

## Output

- `id` (string, required)
- `url` (string, required)
- `name` (string | null, required)
- `variants` (array, required)
- `brand` (string | null, optional)
- `price` (number | null, optional)
- `rating` (number | null, optional)
- `bullets` (array, optional)
- `image_url` (string | null, optional)
- `list_price` (number | null, optional)
- `price_text` (string | null, optional)
- `price_type` (string | null, optional)
- `description` (string | null, optional)
- `max_quantity` (integer | null, optional)
- `review_count` (integer | null, optional)
- `price_valid_until` (string | null, optional)

## FAQ

### What does "Get Macy's product" do?

Read one Macys.com product by id or link: name, brand, description, bullet points, price and regular price in US dollars, price text and deal label, when the price ends, rating, review count, the most per order, image, and every variant (UPC id and number, color, size, in stock, price).

### How do I automatically get Macy's product on macys.com?

Ask an AI agent connected to Reduck to run reduck/macys.com/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/macys.com/get-product

### Is there a macys.com API to get Macy's product?

You do not need one. "Get Macy's product" drives the real macys.com pages in a browser, so it works whether or not macys.com offers an API for this.

### What information do I need to provide?

Required: product.

### What does it return?

It returns id, url, name, brand, price, rating, bullets, variants, image_url, list_price, price_text, price_type, description, max_quantity, review_count, price_valid_until.

### Do I need to be logged in to macys.com?

No. It only uses pages of macys.com that are reachable without signing in.

### Does it change anything on macys.com, or only read data?

It only reads. It looks things up on macys.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/macys.com/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/macys.com/get-product

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/macys.com/get-product
