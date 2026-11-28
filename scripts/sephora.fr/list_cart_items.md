# List Sephora France cart items

Automatically list Sephora France cart items on sephora.fr. Read this browser's sephora.fr basket: each line's id, product, sku, brand, shade or size, quantity, unit and line price in euros, and the review_hash that Remove from Sephora France cart needs, plus the item count and total.

- Site: sephora.fr
- Address: `reduck/sephora.fr/list_cart_items`
- Updated: 2026-11-27 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/sephora.fr/list_cart_items`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/sephora.fr/list_cart_items
```

## Input

It takes no input.

## Output

- `count` (integer, required)
- `lines` (array, required)
- `total` (number | null, optional)

## FAQ

### What does "List Sephora France cart items" do?

Read this browser's sephora.fr basket: each line's id, product, sku, brand, shade or size, quantity, unit and line price in euros, and the review_hash that Remove from Sephora France cart needs, plus the item count and total.

### How do I automatically list Sephora France cart items on sephora.fr?

Ask an AI agent connected to Reduck to run reduck/sephora.fr/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/sephora.fr/list_cart_items

### Is there a sephora.fr API to list Sephora France cart items?

You do not need one. "List Sephora France cart items" drives the real sephora.fr pages in a browser, so it works whether or not sephora.fr offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns count, lines, total.

### Do I need to be logged in to sephora.fr?

No. It only uses pages of sephora.fr that are reachable without signing in.

### Does it change anything on sephora.fr, or only read data?

It only reads. It looks things up on sephora.fr and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/sephora.fr/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/sephora.fr/list_cart_items

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/sephora.fr/list_cart_items
