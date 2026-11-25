# List emag.ro cart items

Automatically list emag.ro cart items on emag.ro. List the items in the emag.ro cart of this browser, as the site holds it: for each line its product id, offer id, name, seller, quantity, unit price and line price in lei (RON), plus the number of items and the products total. The cart is the guest cart of the browser, so no sign-in is needed. An empty cart returns an empty list and a zero count.

- Site: emag.ro
- Address: `reduck/emag.ro/list_cart_items`
- Updated: 2026-11-24 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/emag.ro/list_cart_items`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/emag.ro/list_cart_items
```

## Input

It takes no input.

## Output

- `count` (integer, required): Units in the cart.
- `lines` (array, required)
- `total` (number | null, required): Products total in lei, taxes included, delivery not included.

## FAQ

### What does "List emag.ro cart items" do?

List the items in the emag.ro cart of this browser, as the site holds it: for each line its product id, offer id, name, seller, quantity, unit price and line price in lei (RON), plus the number of items and the products total. The cart is the guest cart of the browser, so no sign-in is needed. An empty cart returns an empty list and a zero count.

### How do I automatically list emag.ro cart items on emag.ro?

Ask an AI agent connected to Reduck to run reduck/emag.ro/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/emag.ro/list_cart_items

### Is there a emag.ro API to list emag.ro cart items?

You do not need one. "List emag.ro cart items" drives the real emag.ro pages in a browser, so it works whether or not emag.ro offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns count, lines, total.

### Do I need to be logged in to emag.ro?

No. It only uses pages of emag.ro that are reachable without signing in.

### Does it change anything on emag.ro, or only read data?

It only reads. It looks things up on emag.ro and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/emag.ro/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/emag.ro/list_cart_items

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/emag.ro/list_cart_items
