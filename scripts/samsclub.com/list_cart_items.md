# List Sam's Club cart items

Automatically list Sam's Club cart items on samsclub.com. List the items in the Sam's Club (samsclub.com, US) cart of this browser, as the site holds it: for each line its line id, product id (the item id), offer id, name, seller (Sam's Club or the marketplace seller), quantity, unit price and line price in US dollars, plus the number of items and the subtotal of the cart, before shipping and tax. The cart is the guest cart of the browser, so no sign-in is needed. An empty cart returns an empty list, a zero count and a zero total. Saved-for-later items are not included.

- Site: samsclub.com
- Address: `reduck/samsclub.com/list_cart_items`
- Updated: 2026-11-26 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/samsclub.com/list_cart_items`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/samsclub.com/list_cart_items
```

## Input

It takes no input.

## Output

- `count` (integer, required): Number of items in the cart, all lines together.
- `lines` (array, required)
- `total` (number | null, required): Subtotal of the cart in US dollars, before shipping and tax.

## FAQ

### What does "List Sam's Club cart items" do?

List the items in the Sam's Club (samsclub.com, US) cart of this browser, as the site holds it: for each line its line id, product id (the item id), offer id, name, seller (Sam's Club or the marketplace seller), quantity, unit price and line price in US dollars, plus the number of items and the subtotal of the cart, before shipping and tax. The cart is the guest cart of the browser, so no sign-in is needed. An empty cart returns an empty list, a zero count and a zero total. Saved-for-later items are not included.

### How do I automatically list Sam's Club cart items on samsclub.com?

Ask an AI agent connected to Reduck to run reduck/samsclub.com/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/samsclub.com/list_cart_items

### Is there a samsclub.com API to list Sam's Club cart items?

You do not need one. "List Sam's Club cart items" drives the real samsclub.com pages in a browser, so it works whether or not samsclub.com offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns count, lines, total.

### Do I need to be logged in to samsclub.com?

No. It only uses pages of samsclub.com that are reachable without signing in.

### Does it change anything on samsclub.com, or only read data?

It only reads. It looks things up on samsclub.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/samsclub.com/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/samsclub.com/list_cart_items

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/samsclub.com/list_cart_items
