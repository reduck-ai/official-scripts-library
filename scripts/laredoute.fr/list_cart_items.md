# List La Redoute cart items

Automatically list La Redoute cart items on laredoute.fr. Read this browser's La Redoute basket: each line's id, product, reference, colour, size, quantity, unit and line price in euros, and the review_hash that Remove from La Redoute cart needs, plus the item count and total to pay.

- Site: laredoute.fr
- Address: `reduck/laredoute.fr/list_cart_items`
- Updated: 2026-11-27 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/laredoute.fr/list_cart_items`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/laredoute.fr/list_cart_items
```

## Input

It takes no input.

## Output

- `count` (integer, required)
- `lines` (array, required)
- `total` (number | null, optional): Total to pay in euros as the basket states it, delivery included.

## FAQ

### What does "List La Redoute cart items" do?

Read this browser's La Redoute basket: each line's id, product, reference, colour, size, quantity, unit and line price in euros, and the review_hash that Remove from La Redoute cart needs, plus the item count and total to pay.

### How do I automatically list La Redoute cart items on laredoute.fr?

Ask an AI agent connected to Reduck to run reduck/laredoute.fr/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/laredoute.fr/list_cart_items

### Is there a laredoute.fr API to list La Redoute cart items?

You do not need one. "List La Redoute cart items" drives the real laredoute.fr pages in a browser, so it works whether or not laredoute.fr offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns count, lines, total.

### Do I need to be logged in to laredoute.fr?

No. It only uses pages of laredoute.fr that are reachable without signing in.

### Does it change anything on laredoute.fr, or only read data?

It only reads. It looks things up on laredoute.fr and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/laredoute.fr/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/laredoute.fr/list_cart_items

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/laredoute.fr/list_cart_items
