# Get Crate & Barrel product

Automatically get Crate & Barrel product on crateandbarrel.com. Read one Crate & Barrel product (crateandbarrel.com, US) from its id or link: name, price, regular price, currency, stock status and delivery message, rating, review count, images, brand, category, description, and its variants (color, size) with the id of each.

- Site: crateandbarrel.com
- Address: `reduck/crateandbarrel.com/get-product`
- Updated: 2026-11-26 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/crateandbarrel.com/get-product`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/crateandbarrel.com/get-product
```

## Input

- `product` (string, required): Product id (the number after /s in a product link, for example 216478) or the product link.

## Output

- `id` (string, required): Product id (SKU).
- `url` (string | null, required)
- `name` (string, required)
- `price` (number | null, required): Current price in USD.
- `currency` (string | null, required)
- `variants` (array, required): Each variant is its own product id. Empty when the product has no color or size choices.
- `availability` (string | null, required): schema.org availability the page gives, for example InStock, OutOfStock, BackOrder.
- `brand` (string | null, optional)
- `images` (array, optional)
- `rating` (number | null, optional)
- `details` (string | null, optional)
- `category` (string | null, optional)
- `family_id` (string | null, optional)
- `list_price` (number | null, optional): Regular price in USD.
- `price_text` (string | null, optional): The price as the site writes it.
- `description` (string | null, optional)
- `review_count` (integer | null, optional)
- `is_backordered` (boolean | null, optional)
- `can_add_to_cart` (boolean, optional): True when the page lets a person add the product to the cart.
- `delivery_message` (string | null, optional): The delivery date the page shows, for example "Arrives Tue, Dec 1".

## FAQ

### What does "Get Crate & Barrel product" do?

Read one Crate & Barrel product (crateandbarrel.com, US) from its id or link: name, price, regular price, currency, stock status and delivery message, rating, review count, images, brand, category, description, and its variants (color, size) with the id of each.

### How do I automatically get Crate & Barrel product on crateandbarrel.com?

Ask an AI agent connected to Reduck to run reduck/crateandbarrel.com/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/crateandbarrel.com/get-product

### Is there a crateandbarrel.com API to get Crate & Barrel product?

You do not need one. "Get Crate & Barrel product" drives the real crateandbarrel.com pages in a browser, so it works whether or not crateandbarrel.com offers an API for this.

### What information do I need to provide?

Required: product.

### What does it return?

It returns id, url, name, brand, price, images, rating, details, category, currency, variants, family_id, list_price, price_text, description, availability, review_count, is_backordered, can_add_to_cart, delivery_message.

### Do I need to be logged in to crateandbarrel.com?

No. It only uses pages of crateandbarrel.com that are reachable without signing in.

### Does it change anything on crateandbarrel.com, or only read data?

It only reads. It looks things up on crateandbarrel.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/crateandbarrel.com/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/crateandbarrel.com/get-product

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/crateandbarrel.com/get-product
