# Get Lowe's product

Automatically get Lowe's product on lowes.com. Read one Lowes.com product page by its link or item id. Returns item_id, item_number, model, url, title, brand, price and struck-through was_price in US dollars, availability by fulfillment method, buyable, marketplace, the seller (Lowe's or the marketplace seller) and seller_id, rating, review_count, images, description, highlights, specifications, category path and variants (each option with its item id and link). An unknown item id, a link Lowe's answers with its "page not found" page, and a link that is not a product page fail with an error that says so. Prices and availability follow the store Lowe's assigns to the browser's location.

- Site: lowes.com
- Address: `reduck/lowes.com/get-product`
- Updated: 2026-11-25 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/lowes.com/get-product`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/lowes.com/get-product
```

## Input

- `url` (string, optional): Lowe's product page link (https://www.lowes.com/pd/<name>/<id>), as returned by Search Lowe's products.
- `item_id` (string, optional): Lowe's item id (item_id of Search Lowe's products). Used when no url is given.

## Output

- `url` (string, required)
- `title` (string | null, required)
- `item_id` (string, required)
- `brand` (string | null, optional)
- `model` (string | null, optional)
- `price` (number | null, optional)
- `store` (string | null, optional)
- `images` (array, optional)
- `rating` (number | null, optional)
- `seller` (string | null, optional): Lowe's, or the marketplace seller that sells and ships the item.
- `buyable` (boolean | null, optional)
- `currency` (string, optional)
- `variants` (array, optional)
- `seller_id` (string | null, optional): Vendor number of the marketplace seller; null when Lowe's sells the item.
- `was_price` (number | null, optional)
- `categories` (array, optional)
- `highlights` (array, optional)
- `description` (string | null, optional)
- `item_number` (string | null, optional)
- `marketplace` (boolean | null, optional)
- `availability` (array, optional)
- `review_count` (integer | null, optional)
- `specifications` (array, optional)

## FAQ

### What does "Get Lowe's product" do?

Read one Lowes.com product page by its link or item id. Returns item_id, item_number, model, url, title, brand, price and struck-through was_price in US dollars, availability by fulfillment method, buyable, marketplace, the seller (Lowe's or the marketplace seller) and seller_id, rating, review_count, images, description, highlights, specifications, category path and variants (each option with its item id and link). An unknown item id, a link Lowe's answers with its "page not found" page, and a link that is not a product page fail with an error that says so. Prices and availability follow the store Lowe's assigns to the browser's location.

### How do I automatically get Lowe's product on lowes.com?

Ask an AI agent connected to Reduck to run reduck/lowes.com/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/lowes.com/get-product

### Is there a lowes.com API to get Lowe's product?

You do not need one. "Get Lowe's product" drives the real lowes.com pages in a browser, so it works whether or not lowes.com offers an API for this.

### What information do I need to provide?

Optional: url, item_id.

### What does it return?

It returns url, brand, model, price, store, title, images, rating, seller, buyable, item_id, currency, variants, seller_id, was_price, categories, highlights, description, item_number, marketplace, availability, review_count, specifications.

### Do I need to be logged in to lowes.com?

No. It only uses pages of lowes.com that are reachable without signing in.

### Does it change anything on lowes.com, or only read data?

It only reads. It looks things up on lowes.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/lowes.com/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/lowes.com/get-product

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/lowes.com/get-product
