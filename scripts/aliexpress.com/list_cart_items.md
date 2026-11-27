# List AliExpress cart items

Automatically list AliExpress cart items on aliexpress.com. List the items in the AliExpress cart of this browser: for each line its line id, product id, offer id (the sku id of the variant), name, seller, quantity, unit price and line price, plus the number of units, the total of the lines (shipping not included) and the currency. The cart is the guest cart of the browser, so no sign-in is needed. An empty cart returns an empty list and a zero count.

- Site: aliexpress.com
- Address: `reduck/aliexpress.com/list_cart_items`
- Updated: 2026-11-26 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/aliexpress.com/list_cart_items`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/aliexpress.com/list_cart_items
```

## Input

It takes no input.

## Output

- `count` (integer, required): Number of units in the cart (the sum of the line quantities).
- `lines` (array, required)
- `total` (number | null, required): Sum of the line prices, shipping not included.
- `currency` (string | null, optional)

## FAQ

### What does "List AliExpress cart items" do?

List the items in the AliExpress cart of this browser: for each line its line id, product id, offer id (the sku id of the variant), name, seller, quantity, unit price and line price, plus the number of units, the total of the lines (shipping not included) and the currency. The cart is the guest cart of the browser, so no sign-in is needed. An empty cart returns an empty list and a zero count.

### How do I automatically list AliExpress cart items on aliexpress.com?

Ask an AI agent connected to Reduck to run reduck/aliexpress.com/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/aliexpress.com/list_cart_items

### Is there a aliexpress.com API to list AliExpress cart items?

You do not need one. "List AliExpress cart items" drives the real aliexpress.com pages in a browser, so it works whether or not aliexpress.com offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns count, lines, total, currency.

### Do I need to be logged in to aliexpress.com?

No. It only uses pages of aliexpress.com that are reachable without signing in.

### Does it change anything on aliexpress.com, or only read data?

It only reads. It looks things up on aliexpress.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/aliexpress.com/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/aliexpress.com/list_cart_items

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/aliexpress.com/list_cart_items
