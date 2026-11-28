# Get Advance Auto Parts product

Automatically get Advance Auto Parts product on shop.advanceautoparts.com. Get one Advance Auto Parts product (shop.advanceautoparts.com) by its product id or product link: name, brand, part number, category path, description, warranty, specifications, images, rating, review count, recommendation percent, price, regular price, list price and sale state in US dollars, the stock status and quantity at the store the site picks for a new visitor, and whether it ships to home or can be picked up in store. The price and stock fields are null when the page did not load them. An unknown product id is refused with an error.

- Site: shop.advanceautoparts.com
- Address: `reduck/shop.advanceautoparts.com/get-product`
- Updated: 2026-11-26 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/shop.advanceautoparts.com/get-product`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/shop.advanceautoparts.com/get-product
```

## Input

- `product` (string, required): Advance Auto Parts product id (for example 10555794, the product_id of Search Advance Auto Parts products) or a shop.advanceautoparts.com product link.

## Output

- `url` (string, required)
- `name` (string, required)
- `images` (array, required)
- `product_id` (string, required)
- `specifications` (array, required)
- `brand` (string | null, optional)
- `price` (number | null, optional): Price the site charges.
- `hazmat` (boolean | null, optional)
- `rating` (number | null, optional): Average rating out of 5.
- `weight` (number | null, optional)
- `on_sale` (boolean | null, optional)
- `category` (string | null, optional)
- `currency` (string | null, optional)
- `store_id` (string | null, optional): The Advance Auto Parts store whose price and stock apply.
- `warranty` (string | null, optional)
- `list_price` (number | null, optional): Manufacturer list price.
- `price_type` (string | null, optional)
- `description` (string | null, optional): Product description as the site writes it, with its HTML.
- `part_number` (string | null, optional)
- `availability` (string | null, optional): Availability the page states, for example InStock.
- `review_count` (integer | null, optional)
- `sale_percent` (number | null, optional)
- `ship_to_home` (boolean | null, optional)
- `store_pickup` (boolean | null, optional)
- `store_status` (string | null, optional): Stock status at the store, as the site gives it.
- `category_path` (array, optional)
- `regular_price` (number | null, optional)
- `store_quantity` (integer | null, optional)
- `recommendation_percent` (number | null, optional)

## FAQ

### What does "Get Advance Auto Parts product" do?

Get one Advance Auto Parts product (shop.advanceautoparts.com) by its product id or product link: name, brand, part number, category path, description, warranty, specifications, images, rating, review count, recommendation percent, price, regular price, list price and sale state in US dollars, the stock status and quantity at the store the site picks for a new visitor, and whether it ships to home or can be picked up in store. The price and stock fields are null when the page did not load them. An unknown product id is refused with an error.

### How do I automatically get Advance Auto Parts product on shop.advanceautoparts.com?

Ask an AI agent connected to Reduck to run reduck/shop.advanceautoparts.com/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/shop.advanceautoparts.com/get-product

### Is there a shop.advanceautoparts.com API to get Advance Auto Parts product?

You do not need one. "Get Advance Auto Parts product" drives the real shop.advanceautoparts.com pages in a browser, so it works whether or not shop.advanceautoparts.com offers an API for this.

### What information do I need to provide?

Required: product.

### What does it return?

It returns url, name, brand, price, hazmat, images, rating, weight, on_sale, category, currency, store_id, warranty, list_price, price_type, product_id, description, part_number, availability, review_count, sale_percent, ship_to_home, store_pickup, store_status, category_path, regular_price, specifications, store_quantity, recommendation_percent.

### Do I need to be logged in to shop.advanceautoparts.com?

No. It only uses pages of shop.advanceautoparts.com that are reachable without signing in.

### Does it change anything on shop.advanceautoparts.com, or only read data?

It only reads. It looks things up on shop.advanceautoparts.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/shop.advanceautoparts.com/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/shop.advanceautoparts.com/get-product

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/shop.advanceautoparts.com/get-product
