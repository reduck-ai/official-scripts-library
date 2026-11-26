# List GameStop cart items

Automatically list GameStop cart items on gamestop.com. List the lines of the GameStop cart of the browser, with quantities, prices and the item subtotal.

- Site: gamestop.com
- Address: `reduck/gamestop.com/list_cart_items`
- Updated: 2026-11-25 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/gamestop.com/list_cart_items`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/gamestop.com/list_cart_items
```

## Input

It takes no input.

## Output

- `count` (integer, required)
- `lines` (array, required)
- `total` (number | null, required)

## FAQ

### What does "List GameStop cart items" do?

List the lines of the GameStop cart of the browser, with quantities, prices and the item subtotal.

### How do I automatically list GameStop cart items on gamestop.com?

Ask an AI agent connected to Reduck to run reduck/gamestop.com/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/gamestop.com/list_cart_items

### Is there a gamestop.com API to list GameStop cart items?

You do not need one. "List GameStop cart items" drives the real gamestop.com pages in a browser, so it works whether or not gamestop.com offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns count, lines, total.

### Do I need to be logged in to gamestop.com?

No. It only uses pages of gamestop.com that are reachable without signing in.

### Does it change anything on gamestop.com, or only read data?

It only reads. It looks things up on gamestop.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/gamestop.com/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/gamestop.com/list_cart_items

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/gamestop.com/list_cart_items
