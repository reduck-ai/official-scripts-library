# List Best Buy cart items

Automatically list Best Buy cart items on bestbuy.com. List the items in this browser's Best Buy (US) cart and the order summary Best Buy computes for it: per item its SKU, title, link, image, quantity, unit and line price, regular price, savings, seller, stock, and the selected delivery (shipping or pickup, ZIP, price and dates); then the subtotal, savings, shipping, tax, fees and order total, which is the all-in price before checkout. The tax is Best Buy's estimate for the cart's ZIP code, given on each item; it is null when Best Buy has not priced the cart yet, and the total then leaves it out. An empty cart returns no items and a null summary. Saved-for-later items are not included.

- Site: bestbuy.com
- Address: `reduck/bestbuy.com/list_cart_items`
- Updated: 2026-11-17 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/bestbuy.com/list_cart_items`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/bestbuy.com/list_cart_items
```

## Input

It takes no input.

## Output

- `items` (array, required)
- `summary` (object | null, required)
- `item_count` (integer, required): Units in the cart, all items.

## FAQ

### What does "List Best Buy cart items" do?

List the items in this browser's Best Buy (US) cart and the order summary Best Buy computes for it: per item its SKU, title, link, image, quantity, unit and line price, regular price, savings, seller, stock, and the selected delivery (shipping or pickup, ZIP, price and dates); then the subtotal, savings, shipping, tax, fees and order total, which is the all-in price before checkout. The tax is Best Buy's estimate for the cart's ZIP code, given on each item; it is null when Best Buy has not priced the cart yet, and the total then leaves it out. An empty cart returns no items and a null summary. Saved-for-later items are not included.

### How do I automatically list Best Buy cart items on bestbuy.com?

Ask an AI agent connected to Reduck to run reduck/bestbuy.com/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/bestbuy.com/list_cart_items

### Is there a bestbuy.com API to list Best Buy cart items?

You do not need one. "List Best Buy cart items" drives the real bestbuy.com pages in a browser, so it works whether or not bestbuy.com offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns items, summary, item_count.

### Do I need to be logged in to bestbuy.com?

No. It only uses pages of bestbuy.com that are reachable without signing in.

### Does it change anything on bestbuy.com, or only read data?

It only reads. It looks things up on bestbuy.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/bestbuy.com/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/bestbuy.com/list_cart_items

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/bestbuy.com/list_cart_items
