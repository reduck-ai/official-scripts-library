# List Kroger cart items

Automatically list Kroger cart items on kroger.com. Read the signed-in Kroger.com cart: item count, total of the prices Kroger shows at the store the cart uses, and each line with its line id, UPC, name, seller, quantity, unit price and line price in US dollars, plus a review_hash per line to pass to Remove from Kroger cart. An empty cart returns no lines.

- Site: kroger.com
- Address: `reduck/kroger.com/list_cart_items`
- Updated: 2026-11-26 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/kroger.com/list_cart_items`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/kroger.com/list_cart_items
```

## Input

It takes no input.

## Output

- `count` (integer, required)
- `lines` (array, required)
- `total` (number | null, required)

## FAQ

### What does "List Kroger cart items" do?

Read the signed-in Kroger.com cart: item count, total of the prices Kroger shows at the store the cart uses, and each line with its line id, UPC, name, seller, quantity, unit price and line price in US dollars, plus a review_hash per line to pass to Remove from Kroger cart. An empty cart returns no lines.

### How do I automatically list Kroger cart items on kroger.com?

Ask an AI agent connected to Reduck to run reduck/kroger.com/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/kroger.com/list_cart_items

### Is there a kroger.com API to list Kroger cart items?

You do not need one. "List Kroger cart items" drives the real kroger.com pages in a browser, so it works whether or not kroger.com offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns count, lines, total.

### Do I need to be logged in to kroger.com?

Yes. It acts as you on kroger.com: in your browser it reuses your session, and on a cloud browser it loads your Auth session cookies for kroger.com.

### Does it change anything on kroger.com, or only read data?

It only reads. It looks things up on kroger.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/kroger.com/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/kroger.com/list_cart_items

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/kroger.com/list_cart_items
