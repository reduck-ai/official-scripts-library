# List Gifi cart items

Automatically list Gifi cart items on gifi.fr. List the items in the Gifi.fr cart of this browser: the unit count, the item subtotal in euros (without delivery) and each line with its line id, product id, offer id, name, seller, quantity, unit price and line price. The cart is the guest cart of the browser, so no sign-in is needed. An empty cart returns no lines and a count of 0.

- Site: gifi.fr
- Address: `reduck/gifi.fr/list_cart_items`
- Updated: 2026-11-25 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/gifi.fr/list_cart_items`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/gifi.fr/list_cart_items
```

## Input

It takes no input.

## Output

- `count` (integer, required): Units in the cart.
- `lines` (array, required)
- `total` (number | null, required): Item subtotal in euros, without delivery. 0 for an empty cart.

## FAQ

### What does "List Gifi cart items" do?

List the items in the Gifi.fr cart of this browser: the unit count, the item subtotal in euros (without delivery) and each line with its line id, product id, offer id, name, seller, quantity, unit price and line price. The cart is the guest cart of the browser, so no sign-in is needed. An empty cart returns no lines and a count of 0.

### How do I automatically list Gifi cart items on gifi.fr?

Ask an AI agent connected to Reduck to run reduck/gifi.fr/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/gifi.fr/list_cart_items

### Is there a gifi.fr API to list Gifi cart items?

You do not need one. "List Gifi cart items" drives the real gifi.fr pages in a browser, so it works whether or not gifi.fr offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns count, lines, total.

### Do I need to be logged in to gifi.fr?

No. It only uses pages of gifi.fr that are reachable without signing in.

### Does it change anything on gifi.fr, or only read data?

It only reads. It looks things up on gifi.fr and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/gifi.fr/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/gifi.fr/list_cart_items

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/gifi.fr/list_cart_items
