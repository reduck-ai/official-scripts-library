# List Electro Dépôt cart items

Automatically list Electro Dépôt cart items on electrodepot.fr. List the items in the shopping cart of this browser on the Electro Dépôt French store (electrodepot.fr): the item count, the items total in euros (taxes included, delivery not included), the currency, and each line with its line id, product id, offer id (always null), name, seller, quantity, unit price and line price. Works as a guest, with no account: the cart lives in the browser, so a new browser has an empty cart. An empty cart returns an empty list.

- Site: electrodepot.fr
- Address: `reduck/electrodepot.fr/list_cart_items`
- Updated: 2026-11-27 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/electrodepot.fr/list_cart_items`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/electrodepot.fr/list_cart_items
```

## Input

It takes no input.

## Output

- `count` (integer, required): Units in the cart.
- `lines` (array, required)
- `total` (number, required): Items total in euros, taxes included, delivery not included.
- `currency` (string, required)

## FAQ

### What does "List Electro Dépôt cart items" do?

List the items in the shopping cart of this browser on the Electro Dépôt French store (electrodepot.fr): the item count, the items total in euros (taxes included, delivery not included), the currency, and each line with its line id, product id, offer id (always null), name, seller, quantity, unit price and line price. Works as a guest, with no account: the cart lives in the browser, so a new browser has an empty cart. An empty cart returns an empty list.

### How do I automatically list Electro Dépôt cart items on electrodepot.fr?

Ask an AI agent connected to Reduck to run reduck/electrodepot.fr/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/electrodepot.fr/list_cart_items

### Is there a electrodepot.fr API to list Electro Dépôt cart items?

You do not need one. "List Electro Dépôt cart items" drives the real electrodepot.fr pages in a browser, so it works whether or not electrodepot.fr offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns count, lines, total, currency.

### Do I need to be logged in to electrodepot.fr?

No. It only uses pages of electrodepot.fr that are reachable without signing in.

### Does it change anything on electrodepot.fr, or only read data?

It only reads. It looks things up on electrodepot.fr and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/electrodepot.fr/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/electrodepot.fr/list_cart_items

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/electrodepot.fr/list_cart_items
