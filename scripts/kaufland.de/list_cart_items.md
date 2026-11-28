# List Kaufland cart items

Automatically list Kaufland cart items on kaufland.de. Read this browser's kaufland.de cart: each line's id, product, offer, seller, attributes, quantity and its limit, unit and line price, shipping fee and delivery window in euros, and the review_hash that Remove from Kaufland cart needs, plus the item count, shipping and total.

- Site: kaufland.de
- Address: `reduck/kaufland.de/list_cart_items`
- Updated: 2026-11-27 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/kaufland.de/list_cart_items`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/kaufland.de/list_cart_items
```

## Input

It takes no input.

## Output

- `count` (integer, required)
- `lines` (array, required)
- `total` (number | null, optional)
- `shipping` (number | null, optional)

## FAQ

### What does "List Kaufland cart items" do?

Read this browser's kaufland.de cart: each line's id, product, offer, seller, attributes, quantity and its limit, unit and line price, shipping fee and delivery window in euros, and the review_hash that Remove from Kaufland cart needs, plus the item count, shipping and total.

### How do I automatically list Kaufland cart items on kaufland.de?

Ask an AI agent connected to Reduck to run reduck/kaufland.de/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/kaufland.de/list_cart_items

### Is there a kaufland.de API to list Kaufland cart items?

You do not need one. "List Kaufland cart items" drives the real kaufland.de pages in a browser, so it works whether or not kaufland.de offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns count, lines, total, shipping.

### Do I need to be logged in to kaufland.de?

No. It only uses pages of kaufland.de that are reachable without signing in.

### Does it change anything on kaufland.de, or only read data?

It only reads. It looks things up on kaufland.de and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/kaufland.de/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/kaufland.de/list_cart_items

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/kaufland.de/list_cart_items
