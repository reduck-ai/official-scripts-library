# List Kohl's cart items

Automatically list Kohl's cart items on kohls.com. Read the Kohls.com cart of this browser: cart id, item count, order total in US dollars as Kohl's states it, and each line with its line id, product id, SKU (offerId), name, color, size, quantity, unit price and line price, plus a review_hash per line to pass to Remove from Kohl's cart. An empty cart returns no lines.

- Site: kohls.com
- Address: `reduck/kohls.com/list_cart_items`
- Updated: 2026-11-27 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/kohls.com/list_cart_items`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/kohls.com/list_cart_items
```

## Input

It takes no input.

## Output

- `count` (integer, required)
- `lines` (array, required)
- `total` (number | null, required)
- `cartId` (string | null, optional)

## FAQ

### What does "List Kohl's cart items" do?

Read the Kohls.com cart of this browser: cart id, item count, order total in US dollars as Kohl's states it, and each line with its line id, product id, SKU (offerId), name, color, size, quantity, unit price and line price, plus a review_hash per line to pass to Remove from Kohl's cart. An empty cart returns no lines.

### How do I automatically list Kohl's cart items on kohls.com?

Ask an AI agent connected to Reduck to run reduck/kohls.com/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/kohls.com/list_cart_items

### Is there a kohls.com API to list Kohl's cart items?

You do not need one. "List Kohl's cart items" drives the real kohls.com pages in a browser, so it works whether or not kohls.com offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns count, lines, total, cartId.

### Do I need to be logged in to kohls.com?

No. It only uses pages of kohls.com that are reachable without signing in.

### Does it change anything on kohls.com, or only read data?

It only reads. It looks things up on kohls.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/kohls.com/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/kohls.com/list_cart_items

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/kohls.com/list_cart_items
