# List Alibaba.com cart items

Automatically list Alibaba.com cart items on alibaba.com. List the items in this browser's Alibaba.com cart: for each line its line id, product id, variant id, title, link, image, supplier (name, company id, country), variant values, quantity, minimum order quantity, unit price, line total, currency and whether it is still available. Also returns the cart's line count, item count, item subtotal, shipping fee, shipping discount, total before tax, display currency and ship-to country. The cart works without sign-in: a browser that is not signed in to Alibaba.com has a cart of its own. An empty cart returns an empty list.

- Site: alibaba.com
- Address: `reduck/alibaba.com/list_cart_items`
- Updated: 2026-11-25 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/alibaba.com/list_cart_items`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/alibaba.com/list_cart_items
```

## Input

It takes no input.

## Output

- `count` (integer, required): Number of items in the cart, all lines' quantities added.
- `lines` (array, required): One line per product variant. Empty for an empty cart.
- `total` (number | null, required): Item subtotal in the display currency that Alibaba.com sets for the browser, shipping not included. 0 for an empty cart.

## FAQ

### What does "List Alibaba.com cart items" do?

List the items in this browser's Alibaba.com cart: for each line its line id, product id, variant id, title, link, image, supplier (name, company id, country), variant values, quantity, minimum order quantity, unit price, line total, currency and whether it is still available. Also returns the cart's line count, item count, item subtotal, shipping fee, shipping discount, total before tax, display currency and ship-to country. The cart works without sign-in: a browser that is not signed in to Alibaba.com has a cart of its own. An empty cart returns an empty list.

### How do I automatically list Alibaba.com cart items on alibaba.com?

Ask an AI agent connected to Reduck to run reduck/alibaba.com/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/alibaba.com/list_cart_items

### Is there a alibaba.com API to list Alibaba.com cart items?

You do not need one. "List Alibaba.com cart items" drives the real alibaba.com pages in a browser, so it works whether or not alibaba.com offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns count, lines, total.

### Do I need to be logged in to alibaba.com?

No. It only uses pages of alibaba.com that are reachable without signing in.

### Does it change anything on alibaba.com, or only read data?

It only reads. It looks things up on alibaba.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/alibaba.com/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/alibaba.com/list_cart_items

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/alibaba.com/list_cart_items
