# List Container Store cart items

Automatically list Container Store cart items on containerstore.com. List the items in the cart of this browser on The Container Store (containerstore.com, US): each line with its line id, product id, variant (SKU) id, name, quantity, unit price after the cart's offers and line price in USD, plus the unit count and the order subtotal. An empty cart gives an empty list. Works as a guest: the cart lives with the browser.

- Site: containerstore.com
- Address: `reduck/containerstore.com/list_cart_items`
- Updated: 2026-11-26 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/containerstore.com/list_cart_items`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/containerstore.com/list_cart_items
```

## Input

It takes no input.

## Output

- `count` (integer, required): Number of units in the cart.
- `lines` (array, required)
- `total` (number | null, required): Order subtotal in USD as the cart shows it: before offers, shipping and tax.

## FAQ

### What does "List Container Store cart items" do?

List the items in the cart of this browser on The Container Store (containerstore.com, US): each line with its line id, product id, variant (SKU) id, name, quantity, unit price after the cart's offers and line price in USD, plus the unit count and the order subtotal. An empty cart gives an empty list. Works as a guest: the cart lives with the browser.

### How do I automatically list Container Store cart items on containerstore.com?

Ask an AI agent connected to Reduck to run reduck/containerstore.com/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/containerstore.com/list_cart_items

### Is there a containerstore.com API to list Container Store cart items?

You do not need one. "List Container Store cart items" drives the real containerstore.com pages in a browser, so it works whether or not containerstore.com offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns count, lines, total.

### Do I need to be logged in to containerstore.com?

No. It only uses pages of containerstore.com that are reachable without signing in.

### Does it change anything on containerstore.com, or only read data?

It only reads. It looks things up on containerstore.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/containerstore.com/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/containerstore.com/list_cart_items

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/containerstore.com/list_cart_items
