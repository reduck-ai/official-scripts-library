# List Myntra bag items

Automatically list Myntra bag items on myntra.com. Read this browser's myntra.com bag: each line's id, product, sku, brand, size, seller, quantity, unit and line price and MRP in rupees, and the review_hash that Remove from Myntra bag needs, plus the item count and total.

- Site: myntra.com
- Address: `reduck/myntra.com/list_cart_items`
- Updated: 2026-11-27 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/myntra.com/list_cart_items`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/myntra.com/list_cart_items
```

## Input

It takes no input.

## Output

- `count` (integer, required)
- `lines` (array, required)
- `total` (number | null, optional)

## FAQ

### What does "List Myntra bag items" do?

Read this browser's myntra.com bag: each line's id, product, sku, brand, size, seller, quantity, unit and line price and MRP in rupees, and the review_hash that Remove from Myntra bag needs, plus the item count and total.

### How do I automatically list Myntra bag items on myntra.com?

Ask an AI agent connected to Reduck to run reduck/myntra.com/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/myntra.com/list_cart_items

### Is there a myntra.com API to list Myntra bag items?

You do not need one. "List Myntra bag items" drives the real myntra.com pages in a browser, so it works whether or not myntra.com offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns count, lines, total.

### Do I need to be logged in to myntra.com?

No. It only uses pages of myntra.com that are reachable without signing in.

### Does it change anything on myntra.com, or only read data?

It only reads. It looks things up on myntra.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/myntra.com/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/myntra.com/list_cart_items

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/myntra.com/list_cart_items
