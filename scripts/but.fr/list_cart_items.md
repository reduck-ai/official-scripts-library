# List BUT.fr cart items

Automatically list BUT.fr cart items on but.fr. List the items in the BUT.fr cart of this browser, as the site holds it: for each line its product id, name, seller, quantity, unit price and line price in euros, plus the number of items and the cart total. The cart is the guest cart of the browser, so no sign-in is needed. An empty cart returns an empty list and a zero count.

- Site: but.fr
- Address: `reduck/but.fr/list_cart_items`
- Updated: 2026-11-24 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/but.fr/list_cart_items`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/but.fr/list_cart_items
```

## Input

It takes no input.

## Output

- `count` (integer, required): Units in the cart.
- `lines` (array, required)
- `total` (number | null, required): Cart total in euros, taxes included.

## FAQ

### What does "List BUT.fr cart items" do?

List the items in the BUT.fr cart of this browser, as the site holds it: for each line its product id, name, seller, quantity, unit price and line price in euros, plus the number of items and the cart total. The cart is the guest cart of the browser, so no sign-in is needed. An empty cart returns an empty list and a zero count.

### How do I automatically list BUT.fr cart items on but.fr?

Ask an AI agent connected to Reduck to run reduck/but.fr/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/but.fr/list_cart_items

### Is there a but.fr API to list BUT.fr cart items?

You do not need one. "List BUT.fr cart items" drives the real but.fr pages in a browser, so it works whether or not but.fr offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns count, lines, total.

### Do I need to be logged in to but.fr?

No. It only uses pages of but.fr that are reachable without signing in.

### Does it change anything on but.fr, or only read data?

It only reads. It looks things up on but.fr and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/but.fr/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/but.fr/list_cart_items

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/but.fr/list_cart_items
