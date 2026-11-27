# List Bed Bath & Beyond cart items

Automatically list Bed Bath & Beyond cart items on bedbathandbeyond.com. List what is in the Bed Bath & Beyond cart of this browser: each line with its product id, option id, name, quantity, unit price and line price, plus the number of items and the cart total in US dollars. An empty cart gives count 0 and no lines.

- Site: bedbathandbeyond.com
- Address: `reduck/bedbathandbeyond.com/list_cart_items`
- Updated: 2026-11-26 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/bedbathandbeyond.com/list_cart_items`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/bedbathandbeyond.com/list_cart_items
```

## Input

It takes no input.

## Output

- `count` (integer, required): The number of items in the cart, all quantities added.
- `lines` (array, required)
- `total` (number | null, required): The cart total in US dollars.

## FAQ

### What does "List Bed Bath & Beyond cart items" do?

List what is in the Bed Bath & Beyond cart of this browser: each line with its product id, option id, name, quantity, unit price and line price, plus the number of items and the cart total in US dollars. An empty cart gives count 0 and no lines.

### How do I automatically list Bed Bath & Beyond cart items on bedbathandbeyond.com?

Ask an AI agent connected to Reduck to run reduck/bedbathandbeyond.com/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/bedbathandbeyond.com/list_cart_items

### Is there a bedbathandbeyond.com API to list Bed Bath & Beyond cart items?

You do not need one. "List Bed Bath & Beyond cart items" drives the real bedbathandbeyond.com pages in a browser, so it works whether or not bedbathandbeyond.com offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns count, lines, total.

### Do I need to be logged in to bedbathandbeyond.com?

No. It only uses pages of bedbathandbeyond.com that are reachable without signing in.

### Does it change anything on bedbathandbeyond.com, or only read data?

It only reads. It looks things up on bedbathandbeyond.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/bedbathandbeyond.com/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/bedbathandbeyond.com/list_cart_items

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/bedbathandbeyond.com/list_cart_items
