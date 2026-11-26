# List Boulanger cart items

Automatically list Boulanger cart items on boulanger.com. List the items in the Boulanger.com cart: for each line its line id, product id, offer id, name, seller, quantity, unit price and line price, plus the item count and the total in euros. An empty cart returns count 0, total 0 and no lines. Works as a guest: the cart lives with the browser.

- Site: boulanger.com
- Address: `reduck/boulanger.com/list_cart_items`
- Updated: 2026-11-25 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/boulanger.com/list_cart_items`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/boulanger.com/list_cart_items
```

## Input

It takes no input.

## Output

- `count` (integer, required)
- `lines` (array, required)
- `total` (number | null, required): Euros, items only (no shipping); 0 for an empty cart.

## FAQ

### What does "List Boulanger cart items" do?

List the items in the Boulanger.com cart: for each line its line id, product id, offer id, name, seller, quantity, unit price and line price, plus the item count and the total in euros. An empty cart returns count 0, total 0 and no lines. Works as a guest: the cart lives with the browser.

### How do I automatically list Boulanger cart items on boulanger.com?

Ask an AI agent connected to Reduck to run reduck/boulanger.com/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/boulanger.com/list_cart_items

### Is there a boulanger.com API to list Boulanger cart items?

You do not need one. "List Boulanger cart items" drives the real boulanger.com pages in a browser, so it works whether or not boulanger.com offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns count, lines, total.

### Do I need to be logged in to boulanger.com?

No. It only uses pages of boulanger.com that are reachable without signing in.

### Does it change anything on boulanger.com, or only read data?

It only reads. It looks things up on boulanger.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/boulanger.com/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/boulanger.com/list_cart_items

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/boulanger.com/list_cart_items
