# List Overstock cart items

Automatically list Overstock cart items on overstock.com. List what is in the Overstock cart of this browser: each line with its id, product id, option id, name, quantity, unit price and line price, plus the number of items and the estimated cart total in US dollars. An empty cart gives count 0 and no lines.

- Site: overstock.com
- Address: `reduck/overstock.com/list_cart_items`
- Updated: 2026-11-26 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/overstock.com/list_cart_items`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/overstock.com/list_cart_items
```

## Input

It takes no input.

## Output

- `count` (integer, required): The number of items in the cart, all quantities added.
- `lines` (array, required)
- `total` (number | null, required): The estimated cart total in US dollars, before taxes.

## FAQ

### What does "List Overstock cart items" do?

List what is in the Overstock cart of this browser: each line with its id, product id, option id, name, quantity, unit price and line price, plus the number of items and the estimated cart total in US dollars. An empty cart gives count 0 and no lines.

### How do I automatically list Overstock cart items on overstock.com?

Ask an AI agent connected to Reduck to run reduck/overstock.com/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/overstock.com/list_cart_items

### Is there a overstock.com API to list Overstock cart items?

You do not need one. "List Overstock cart items" drives the real overstock.com pages in a browser, so it works whether or not overstock.com offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns count, lines, total.

### Do I need to be logged in to overstock.com?

No. It only uses pages of overstock.com that are reachable without signing in.

### Does it change anything on overstock.com, or only read data?

It only reads. It looks things up on overstock.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/overstock.com/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/overstock.com/list_cart_items

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/overstock.com/list_cart_items
