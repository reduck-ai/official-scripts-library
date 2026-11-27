# List Newegg cart items

Automatically list Newegg cart items on newegg.com. List the items in your Newegg (newegg.com) cart: for each line its item number, name, seller, quantity, unit price and line price, plus the item count and total in USD. An empty cart returns count 0 and an empty list. Saved-for-later items are not included.

- Site: newegg.com
- Address: `reduck/newegg.com/list_cart_items`
- Updated: 2026-11-25 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/newegg.com/list_cart_items`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/newegg.com/list_cart_items
```

## Input

It takes no input.

## Output

- `count` (integer, required): Total quantity across the lines.
- `lines` (array, required)
- `total` (number | null, optional): Cart total in USD as the cart shows it; null for an empty cart.

## FAQ

### What does "List Newegg cart items" do?

List the items in your Newegg (newegg.com) cart: for each line its item number, name, seller, quantity, unit price and line price, plus the item count and total in USD. An empty cart returns count 0 and an empty list. Saved-for-later items are not included.

### How do I automatically list Newegg cart items on newegg.com?

Ask an AI agent connected to Reduck to run reduck/newegg.com/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/newegg.com/list_cart_items

### Is there a newegg.com API to list Newegg cart items?

You do not need one. "List Newegg cart items" drives the real newegg.com pages in a browser, so it works whether or not newegg.com offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns count, lines, total.

### Do I need to be logged in to newegg.com?

No. It only uses pages of newegg.com that are reachable without signing in.

### Does it change anything on newegg.com, or only read data?

It only reads. It looks things up on newegg.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/newegg.com/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/newegg.com/list_cart_items

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/newegg.com/list_cart_items
