# Get Office Depot product

Automatically get Office Depot product on officedepot.com. Read one OfficeDepot.com product page by its link or item number. Returns the item number, link, title, brand, manufacturer part number, selling, regular and list price in US dollars, unit, stock quantity, delivery days, whether it ships only, is pickup only or can be added to the cart, the seller (Office Depot or the marketplace seller) and its offer id, rating, review count, images, description, highlights, specifications and category path. An item number Office Depot does not know and a link that is not a product page fail with an error that says so. Stock and delivery estimates follow the store Office Depot assigns to a new guest browser (store_id).

- Site: officedepot.com
- Address: `reduck/officedepot.com/get-product`
- Updated: 2026-11-26 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/officedepot.com/get-product`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/officedepot.com/get-product
```

## Input

- `url` (string, optional): Office Depot product page link (https://www.officedepot.com/a/products/<number>/<name>/), as returned by Search Office Depot products.
- `product_id` (string, optional): Office Depot item number (product_id of Search Office Depot products). Used when no url is given.

## Output

- `url` (string, required)
- `title` (string | null, required)
- `product_id` (string, required)
- `unit` (string | null, optional)
- `brand` (string | null, optional)
- `model` (string | null, optional): Manufacturer part number.
- `price` (number | null, optional): Selling price in US dollars.
- `images` (array, optional)
- `rating` (number | null, optional)
- `seller` (string | null, optional): Office Depot, or the marketplace seller.
- `currency` (string, optional)
- `offer_id` (string | null, optional): Marketplace offer id; null when Office Depot sells the item.
- `store_id` (string | null, optional)
- `warnings` (array, optional)
- `categories` (array, optional)
- `highlights` (array, optional)
- `list_price` (number | null, optional)
- `description` (string | null, optional)
- `pickup_only` (boolean | null, optional)
- `availability` (string | null, optional): Availability as the page gives it, e.g. InStock or OutOfStock.
- `review_count` (integer | null, optional)
- `delivery_days` (string | null, optional)
- `delivery_only` (boolean | null, optional)
- `regular_price` (number | null, optional)
- `specifications` (array, optional)
- `stock_quantity` (integer | null, optional)
- `can_add_to_cart` (boolean | null, optional)

## FAQ

### What does "Get Office Depot product" do?

Read one OfficeDepot.com product page by its link or item number. Returns the item number, link, title, brand, manufacturer part number, selling, regular and list price in US dollars, unit, stock quantity, delivery days, whether it ships only, is pickup only or can be added to the cart, the seller (Office Depot or the marketplace seller) and its offer id, rating, review count, images, description, highlights, specifications and category path. An item number Office Depot does not know and a link that is not a product page fail with an error that says so. Stock and delivery estimates follow the store Office Depot assigns to a new guest browser (store_id).

### How do I automatically get Office Depot product on officedepot.com?

Ask an AI agent connected to Reduck to run reduck/officedepot.com/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/officedepot.com/get-product

### Is there a officedepot.com API to get Office Depot product?

You do not need one. "Get Office Depot product" drives the real officedepot.com pages in a browser, so it works whether or not officedepot.com offers an API for this.

### What information do I need to provide?

Optional: url, product_id.

### What does it return?

It returns url, unit, brand, model, price, title, images, rating, seller, currency, offer_id, store_id, warnings, categories, highlights, list_price, product_id, description, pickup_only, availability, review_count, delivery_days, delivery_only, regular_price, specifications, stock_quantity, can_add_to_cart.

### Do I need to be logged in to officedepot.com?

No. It only uses pages of officedepot.com that are reachable without signing in.

### Does it change anything on officedepot.com, or only read data?

It only reads. It looks things up on officedepot.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/officedepot.com/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/officedepot.com/get-product

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/officedepot.com/get-product
