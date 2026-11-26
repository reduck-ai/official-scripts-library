# List Lowe's cart items

Automatically list Lowe's cart items on lowes.com. List the items in the Lowes.com cart of this browser: for each line its line id, product id (the item id), offer id (always null), name, seller (Lowe's or the marketplace seller), quantity, unit price and line price in US dollars, plus the number of items and the subtotal of the cart, before tax and delivery. The cart is the guest cart of the browser, so no sign-in is needed. An empty cart returns an empty list and a zero count. Saved-for-later items are not included.

- Site: lowes.com
- Address: `reduck/lowes.com/list_cart_items`
- Updated: 2026-11-25 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/lowes.com/list_cart_items`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/lowes.com/list_cart_items
```

## Input

It takes no input.

## Output

- `count` (integer, required): Number of units in the cart, all lines together.
- `lines` (array, required)
- `total` (number | null, required): Subtotal of the cart in US dollars, before tax and delivery.

## FAQ

### What does "List Lowe's cart items" do?

List the items in the Lowes.com cart of this browser: for each line its line id, product id (the item id), offer id (always null), name, seller (Lowe's or the marketplace seller), quantity, unit price and line price in US dollars, plus the number of items and the subtotal of the cart, before tax and delivery. The cart is the guest cart of the browser, so no sign-in is needed. An empty cart returns an empty list and a zero count. Saved-for-later items are not included.

### How do I automatically list Lowe's cart items on lowes.com?

Ask an AI agent connected to Reduck to run reduck/lowes.com/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/lowes.com/list_cart_items

### Is there a lowes.com API to list Lowe's cart items?

You do not need one. "List Lowe's cart items" drives the real lowes.com pages in a browser, so it works whether or not lowes.com offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns count, lines, total.

### Do I need to be logged in to lowes.com?

No. It only uses pages of lowes.com that are reachable without signing in.

### Does it change anything on lowes.com, or only read data?

It only reads. It looks things up on lowes.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/lowes.com/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/lowes.com/list_cart_items

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/lowes.com/list_cart_items
