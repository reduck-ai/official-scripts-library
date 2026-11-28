# List the items in the Petco cart

Automatically list the items in the Petco cart on petco.com. List the items in the Petco (petco.com, US) cart of this browser, as the site holds it: for each line its line id, product id, offer id (the item number of the size), name, seller (always Petco), quantity, unit price and line price in US dollars, plus the number of units and the subtotal before shipping and tax. The cart is the guest cart of the browser, so no sign-in is needed. An empty cart returns an empty list, a zero count and a zero total. Use a managed browser with country US.

- Site: petco.com
- Address: `reduck/petco.com/list_cart_items`
- Updated: 2026-11-27 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/petco.com/list_cart_items`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/petco.com/list_cart_items
```

## Input

It takes no input.

## Output

- `count` (integer, required): Number of units in the cart.
- `lines` (array, required)
- `total` (number | null, required): Subtotal in US dollars, before shipping and tax.

## FAQ

### What does "List the items in the Petco cart" do?

List the items in the Petco (petco.com, US) cart of this browser, as the site holds it: for each line its line id, product id, offer id (the item number of the size), name, seller (always Petco), quantity, unit price and line price in US dollars, plus the number of units and the subtotal before shipping and tax. The cart is the guest cart of the browser, so no sign-in is needed. An empty cart returns an empty list, a zero count and a zero total. Use a managed browser with country US.

### How do I automatically list the items in the Petco cart on petco.com?

Ask an AI agent connected to Reduck to run reduck/petco.com/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/petco.com/list_cart_items

### Is there a petco.com API to list the items in the Petco cart?

You do not need one. "List the items in the Petco cart" drives the real petco.com pages in a browser, so it works whether or not petco.com offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns count, lines, total.

### Do I need to be logged in to petco.com?

No. It only uses pages of petco.com that are reachable without signing in.

### Does it change anything on petco.com, or only read data?

It only reads. It looks things up on petco.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/petco.com/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/petco.com/list_cart_items

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/petco.com/list_cart_items
