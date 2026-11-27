# List Office Depot cart items

Automatically list Office Depot cart items on officedepot.com. List the items in the OfficeDepot.com cart of this browser, as the site holds it: for each line its line id, product id (the item number), offer id (the marketplace offer, null when Office Depot sells it), name, seller (Office Depot or the marketplace seller), quantity, unit price and line price in US dollars, plus the number of items and the subtotal of the cart, before tax and delivery. The cart is the guest cart of the browser, so no sign-in is needed. An empty cart returns an empty list and a zero count. Saved-for-later items are not included.

- Site: officedepot.com
- Address: `reduck/officedepot.com/list_cart_items`
- Updated: 2026-11-26 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/officedepot.com/list_cart_items`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/officedepot.com/list_cart_items
```

## Input

It takes no input.

## Output

- `count` (integer, required): Number of units in the cart, all lines together.
- `lines` (array, required)
- `total` (number | null, required): Subtotal of the cart in US dollars, before tax and delivery.

## FAQ

### What does "List Office Depot cart items" do?

List the items in the OfficeDepot.com cart of this browser, as the site holds it: for each line its line id, product id (the item number), offer id (the marketplace offer, null when Office Depot sells it), name, seller (Office Depot or the marketplace seller), quantity, unit price and line price in US dollars, plus the number of items and the subtotal of the cart, before tax and delivery. The cart is the guest cart of the browser, so no sign-in is needed. An empty cart returns an empty list and a zero count. Saved-for-later items are not included.

### How do I automatically list Office Depot cart items on officedepot.com?

Ask an AI agent connected to Reduck to run reduck/officedepot.com/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/officedepot.com/list_cart_items

### Is there a officedepot.com API to list Office Depot cart items?

You do not need one. "List Office Depot cart items" drives the real officedepot.com pages in a browser, so it works whether or not officedepot.com offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns count, lines, total.

### Do I need to be logged in to officedepot.com?

No. It only uses pages of officedepot.com that are reachable without signing in.

### Does it change anything on officedepot.com, or only read data?

It only reads. It looks things up on officedepot.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/officedepot.com/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/officedepot.com/list_cart_items

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/officedepot.com/list_cart_items
