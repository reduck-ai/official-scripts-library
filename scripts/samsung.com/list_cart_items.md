# List Samsung cart items

Automatically list Samsung cart items on samsung.com. List the items in the Samsung US store (samsung.com/us) cart of this browser, as the site holds it: for each line its line id, product id (the model code), offer id (the same model code), name, seller (always Samsung), quantity, unit price and line price in US dollars, plus the number of items and the subtotal of the cart, before tax and delivery. The cart is the guest cart of the browser, so no sign-in is needed. An empty cart returns an empty list and a zero count.

- Site: samsung.com
- Address: `reduck/samsung.com/list_cart_items`
- Updated: 2026-11-26 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/samsung.com/list_cart_items`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/samsung.com/list_cart_items
```

## Input

It takes no input.

## Output

- `count` (integer, required): Number of units in the cart, all lines together.
- `lines` (array, required)
- `total` (number | null, required): Subtotal of the cart in US dollars, before tax and delivery.

## FAQ

### What does "List Samsung cart items" do?

List the items in the Samsung US store (samsung.com/us) cart of this browser, as the site holds it: for each line its line id, product id (the model code), offer id (the same model code), name, seller (always Samsung), quantity, unit price and line price in US dollars, plus the number of items and the subtotal of the cart, before tax and delivery. The cart is the guest cart of the browser, so no sign-in is needed. An empty cart returns an empty list and a zero count.

### How do I automatically list Samsung cart items on samsung.com?

Ask an AI agent connected to Reduck to run reduck/samsung.com/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/samsung.com/list_cart_items

### Is there a samsung.com API to list Samsung cart items?

You do not need one. "List Samsung cart items" drives the real samsung.com pages in a browser, so it works whether or not samsung.com offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns count, lines, total.

### Do I need to be logged in to samsung.com?

No. It only uses pages of samsung.com that are reachable without signing in.

### Does it change anything on samsung.com, or only read data?

It only reads. It looks things up on samsung.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/samsung.com/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/samsung.com/list_cart_items

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/samsung.com/list_cart_items
