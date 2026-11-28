# Remove product from Electro Dépôt cart

Automatically remove product from Electro Dépôt cart on electrodepot.fr. Remove a product from the shopping cart of this browser on the Electro Dépôt French store (electrodepot.fr), by its product id (as List Electro Dépôt cart items returns it), whatever its quantity, as the cart page's delete button does. Pass a line id to remove one line only. Returns removed and the cart as it is after the removal: item count, items total in euros, currency, and each line with its line id, product id, offer id, name, seller, quantity, unit price and line price. A product that is not in the cart gives removed false and the cart unchanged, not an error. Works as a guest, with no account.

- Site: electrodepot.fr
- Address: `reduck/electrodepot.fr/remove_from_cart`
- Updated: 2026-11-27 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/electrodepot.fr/remove_from_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/electrodepot.fr/remove_from_cart
```

## Input

- `product` (string, required): Product id of a cart line, from List Electro Dépôt cart items (for example 36453).
- `lineId` (string, optional): Line id from List Electro Dépôt cart items, to remove that line only.

## Output

- `count` (integer, required): Units in the cart.
- `lines` (array, required)
- `total` (number, required): Items total in euros, taxes included, delivery not included.
- `removed` (boolean, required): False when the product was not in the cart.
- `currency` (string, required)

## FAQ

### What does "Remove product from Electro Dépôt cart" do?

Remove a product from the shopping cart of this browser on the Electro Dépôt French store (electrodepot.fr), by its product id (as List Electro Dépôt cart items returns it), whatever its quantity, as the cart page's delete button does. Pass a line id to remove one line only. Returns removed and the cart as it is after the removal: item count, items total in euros, currency, and each line with its line id, product id, offer id, name, seller, quantity, unit price and line price. A product that is not in the cart gives removed false and the cart unchanged, not an error. Works as a guest, with no account.

### How do I automatically remove product from Electro Dépôt cart on electrodepot.fr?

Ask an AI agent connected to Reduck to run reduck/electrodepot.fr/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/electrodepot.fr/remove_from_cart

### Is there a electrodepot.fr API to remove product from Electro Dépôt cart?

You do not need one. "Remove product from Electro Dépôt cart" drives the real electrodepot.fr pages in a browser, so it works whether or not electrodepot.fr offers an API for this.

### What information do I need to provide?

Required: product. Optional: lineId.

### What does it return?

It returns count, lines, total, removed, currency.

### Do I need to be logged in to electrodepot.fr?

No. It only uses pages of electrodepot.fr that are reachable without signing in.

### Does it change anything on electrodepot.fr, or only read data?

It makes changes on electrodepot.fr, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/electrodepot.fr/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/electrodepot.fr/remove_from_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/electrodepot.fr/remove_from_cart
