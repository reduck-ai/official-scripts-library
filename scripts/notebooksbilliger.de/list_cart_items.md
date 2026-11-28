# List notebooksbilliger.de cart items

Automatically list notebooksbilliger.de cart items on notebooksbilliger.de. Read the notebooksbilliger.de cart of this browser: item count, total of the item prices, and each line with its product id, article number, name, quantity, unit price and line price in euros, plus a review_hash per line to pass to Remove from notebooksbilliger.de cart. Free add-ons the site puts in the cart with a product are lines too. An empty cart returns no lines. On a browser that does not keep the site's cookies between runs, the cart is empty each time.

- Site: notebooksbilliger.de
- Address: `reduck/notebooksbilliger.de/list_cart_items`
- Updated: 2026-11-27 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/notebooksbilliger.de/list_cart_items`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/notebooksbilliger.de/list_cart_items
```

## Input

It takes no input.

## Output

- `count` (integer, required)
- `lines` (array, required)
- `total` (number | null, required)

## FAQ

### What does "List notebooksbilliger.de cart items" do?

Read the notebooksbilliger.de cart of this browser: item count, total of the item prices, and each line with its product id, article number, name, quantity, unit price and line price in euros, plus a review_hash per line to pass to Remove from notebooksbilliger.de cart. Free add-ons the site puts in the cart with a product are lines too. An empty cart returns no lines. On a browser that does not keep the site's cookies between runs, the cart is empty each time.

### How do I automatically list notebooksbilliger.de cart items on notebooksbilliger.de?

Ask an AI agent connected to Reduck to run reduck/notebooksbilliger.de/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/notebooksbilliger.de/list_cart_items

### Is there a notebooksbilliger.de API to list notebooksbilliger.de cart items?

You do not need one. "List notebooksbilliger.de cart items" drives the real notebooksbilliger.de pages in a browser, so it works whether or not notebooksbilliger.de offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns count, lines, total.

### Do I need to be logged in to notebooksbilliger.de?

No. It only uses pages of notebooksbilliger.de that are reachable without signing in.

### Does it change anything on notebooksbilliger.de, or only read data?

It only reads. It looks things up on notebooksbilliger.de and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/notebooksbilliger.de/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/notebooksbilliger.de/list_cart_items

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/notebooksbilliger.de/list_cart_items
