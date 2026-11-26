# List Cdiscount cart items

Automatically list Cdiscount cart items on cdiscount.com. List the items in the Cdiscount.com cart: for each line its line id, sku, offer id, name, seller, quantity, unit price and line price, plus the article count and the total in euros. An empty cart returns count 0, total 0 and no lines. Works as a guest: the cart lives with the browser.

- Site: cdiscount.com
- Address: `reduck/cdiscount.com/list_cart_items`
- Updated: 2026-11-25 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/cdiscount.com/list_cart_items`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/cdiscount.com/list_cart_items
```

## Input

It takes no input.

## Output

- `count` (integer, required): Number of articles (sum of quantities).
- `lines` (array, required)
- `total` (number | null, required): Cart total in euros as Cdiscount computes it; 0 for an empty cart.

## FAQ

### What does "List Cdiscount cart items" do?

List the items in the Cdiscount.com cart: for each line its line id, sku, offer id, name, seller, quantity, unit price and line price, plus the article count and the total in euros. An empty cart returns count 0, total 0 and no lines. Works as a guest: the cart lives with the browser.

### How do I automatically list Cdiscount cart items on cdiscount.com?

Ask an AI agent connected to Reduck to run reduck/cdiscount.com/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/cdiscount.com/list_cart_items

### Is there a cdiscount.com API to list Cdiscount cart items?

You do not need one. "List Cdiscount cart items" drives the real cdiscount.com pages in a browser, so it works whether or not cdiscount.com offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns count, lines, total.

### Do I need to be logged in to cdiscount.com?

No. It only uses pages of cdiscount.com that are reachable without signing in.

### Does it change anything on cdiscount.com, or only read data?

It only reads. It looks things up on cdiscount.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/cdiscount.com/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/cdiscount.com/list_cart_items

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/cdiscount.com/list_cart_items
