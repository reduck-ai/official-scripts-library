# Get Newegg product

Automatically get Newegg product on newegg.com. Read one newegg.com product from its item number or product link: name, price, list price, stock, rating, review count, brand, images, and the seller (Newegg or a marketplace store).

- Site: newegg.com
- Address: `reduck/newegg.com/get-product`
- Updated: 2026-11-25 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/newegg.com/get-product`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/newegg.com/get-product
```

## Input

- `item` (string, required): Newegg item number (e.g. N82E16820242902, 20-242-902 or a marketplace number like 9SIC7ABKZW2884), or a product URL; search-products returns it.

## Output

- `url` (string, required)
- `item` (string, required): Newegg item number of the product shown; pass it to add_to_cart.
- `title` (string | null, required)
- `requested_item` (string, required)
- `brand` (string | null, optional)
- `model` (string | null, optional)
- `price` (number | null, optional): Current price in USD.
- `images` (array, optional)
- `rating` (number | null, optional)
- `seller` (string | null, optional): Marketplace seller; null when sold by Newegg.
- `bullets` (array, optional): The product's feature bullets.
- `category` (array, optional)
- `currency` (string, optional)
- `in_stock` (boolean | null, optional)
- `variants` (array, optional): Option groups (style, capacity...) with, for each option, the item numbers that carry it.
- `was_price` (number | null, optional): Higher original price when Newegg shows one.
- `description` (string | null, optional): Newegg's short product description, when it has one.
- `item_number` (string, optional)
- `review_count` (integer | null, optional)
- `limit_quantity` (integer | null, optional): Most units one order may hold, when Newegg limits it.
- `sold_by_newegg` (boolean, optional)
- `specifications` (array, optional)

## FAQ

### What does "Get Newegg product" do?

Read one newegg.com product from its item number or product link: name, price, list price, stock, rating, review count, brand, images, and the seller (Newegg or a marketplace store).

### How do I automatically get Newegg product on newegg.com?

Ask an AI agent connected to Reduck to run reduck/newegg.com/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/newegg.com/get-product

### Is there a newegg.com API to get Newegg product?

You do not need one. "Get Newegg product" drives the real newegg.com pages in a browser, so it works whether or not newegg.com offers an API for this.

### What information do I need to provide?

Required: item.

### What does it return?

It returns url, item, brand, model, price, title, images, rating, seller, bullets, category, currency, in_stock, variants, was_price, description, item_number, review_count, limit_quantity, requested_item, sold_by_newegg, specifications.

### Do I need to be logged in to newegg.com?

No. It only uses pages of newegg.com that are reachable without signing in.

### Does it change anything on newegg.com, or only read data?

It only reads. It looks things up on newegg.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/newegg.com/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/newegg.com/get-product

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/newegg.com/get-product
