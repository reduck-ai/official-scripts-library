# List Castorama cart items

Automatically list Castorama cart items on castorama.fr. List the items in the castorama.fr cart of this browser, as the site holds it: for each line its product id, offer id, name, seller, quantity, unit price and line price in euros, plus the number of items and the cart total in euros, delivery not included. The cart is the guest cart of the browser, so no sign-in is needed. An empty cart returns an empty list and a zero count.

- Site: castorama.fr
- Address: `reduck/castorama.fr/list_cart_items`
- Updated: 2026-11-24 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/castorama.fr/list_cart_items`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/castorama.fr/list_cart_items
```

## Input

It takes no input.

## Output

- `count` (integer, required): Units in the cart.
- `lines` (array, required)
- `total` (number | null, required): Cart total in euros, taxes included, delivery not included.

## FAQ

### What does "List Castorama cart items" do?

List the items in the castorama.fr cart of this browser, as the site holds it: for each line its product id, offer id, name, seller, quantity, unit price and line price in euros, plus the number of items and the cart total in euros, delivery not included. The cart is the guest cart of the browser, so no sign-in is needed. An empty cart returns an empty list and a zero count.

### How do I automatically list Castorama cart items on castorama.fr?

Ask an AI agent connected to Reduck to run reduck/castorama.fr/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/castorama.fr/list_cart_items

### Is there a castorama.fr API to list Castorama cart items?

You do not need one. "List Castorama cart items" drives the real castorama.fr pages in a browser, so it works whether or not castorama.fr offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns count, lines, total.

### Do I need to be logged in to castorama.fr?

No. It only uses pages of castorama.fr that are reachable without signing in.

### Does it change anything on castorama.fr, or only read data?

It only reads. It looks things up on castorama.fr and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/castorama.fr/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/castorama.fr/list_cart_items

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/castorama.fr/list_cart_items
