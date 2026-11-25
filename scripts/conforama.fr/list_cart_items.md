# List Conforama cart items

Automatically list Conforama cart items on conforama.fr. List the items in the Conforama cart: for each line its product id, offer id, name, seller, quantity, unit price and line price in euros, plus the number of items and the cart total. Works as a guest, with no account. An empty cart returns an empty list, a zero count and a zero total.

- Site: conforama.fr
- Address: `reduck/conforama.fr/list_cart_items`
- Updated: 2026-11-24 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/conforama.fr/list_cart_items`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/conforama.fr/list_cart_items
```

## Input

It takes no input.

## Output

- `count` (integer, required): Units in the cart.
- `lines` (array, required)
- `total` (number | null, required): Cart total in euros, taxes included.

## FAQ

### What does "List Conforama cart items" do?

List the items in the Conforama cart: for each line its product id, offer id, name, seller, quantity, unit price and line price in euros, plus the number of items and the cart total. Works as a guest, with no account. An empty cart returns an empty list, a zero count and a zero total.

### How do I automatically list Conforama cart items on conforama.fr?

Ask an AI agent connected to Reduck to run reduck/conforama.fr/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/conforama.fr/list_cart_items

### Is there a conforama.fr API to list Conforama cart items?

You do not need one. "List Conforama cart items" drives the real conforama.fr pages in a browser, so it works whether or not conforama.fr offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns count, lines, total.

### Do I need to be logged in to conforama.fr?

No. It only uses pages of conforama.fr that are reachable without signing in.

### Does it change anything on conforama.fr, or only read data?

It only reads. It looks things up on conforama.fr and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/conforama.fr/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/conforama.fr/list_cart_items

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/conforama.fr/list_cart_items
