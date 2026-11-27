# List Crate & Barrel cart items

Automatically list Crate & Barrel cart items on crateandbarrel.com. List the items in the Crate & Barrel cart (crateandbarrel.com, US) of this browser: each line with its product id, name, quantity, unit price and line price, the number of items and the item subtotal (no tax, no shipping).

- Site: crateandbarrel.com
- Address: `reduck/crateandbarrel.com/list_cart_items`
- Updated: 2026-11-26 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/crateandbarrel.com/list_cart_items`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/crateandbarrel.com/list_cart_items
```

## Input

It takes no input.

## Output

- `count` (integer, required): Number of items (units) in the cart.
- `lines` (array, required)
- `total` (number | null, required): Item subtotal in USD, without tax or shipping.

## FAQ

### What does "List Crate & Barrel cart items" do?

List the items in the Crate & Barrel cart (crateandbarrel.com, US) of this browser: each line with its product id, name, quantity, unit price and line price, the number of items and the item subtotal (no tax, no shipping).

### How do I automatically list Crate & Barrel cart items on crateandbarrel.com?

Ask an AI agent connected to Reduck to run reduck/crateandbarrel.com/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/crateandbarrel.com/list_cart_items

### Is there a crateandbarrel.com API to list Crate & Barrel cart items?

You do not need one. "List Crate & Barrel cart items" drives the real crateandbarrel.com pages in a browser, so it works whether or not crateandbarrel.com offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns count, lines, total.

### Do I need to be logged in to crateandbarrel.com?

No. It only uses pages of crateandbarrel.com that are reachable without signing in.

### Does it change anything on crateandbarrel.com, or only read data?

It only reads. It looks things up on crateandbarrel.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/crateandbarrel.com/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/crateandbarrel.com/list_cart_items

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/crateandbarrel.com/list_cart_items
