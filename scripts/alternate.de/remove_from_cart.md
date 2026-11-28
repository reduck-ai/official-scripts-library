# Remove a product from the Alternate cart

Automatically remove a product from the Alternate cart on alternate.de. Remove a product from the shopping cart of this browser on Alternate Germany (alternate.de, the German store), from its Alternate product id (Art.-Nr.) or product page link, whatever its quantity, as the cart page's delete button does. Returns removed and the cart after it: each line with its product id, name, quantity, unit price and line price in euros (VAT included), the item count, the items total and the currency. A product that is not in the cart gives removed false and the cart unchanged, not an error. Works as a guest, with no account.

- Site: alternate.de
- Address: `reduck/alternate.de/remove_from_cart`
- Updated: 2026-11-27 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/alternate.de/remove_from_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/alternate.de/remove_from_cart
```

## Input

- `product` (string, required): An Alternate product id (Art.-Nr.) as List Alternate cart items returns it, for example 1864243, or an alternate.de product page link.

## Output

- `count` (integer, required): Units in the cart after the removal.
- `lines` (array, required)
- `total` (number | null, required): Total of the item lines in euros, VAT included, delivery not included.
- `removed` (boolean, required): True when this run removed the product, false when it was not in the cart.
- `currency` (string, required)

## FAQ

### What does "Remove a product from the Alternate cart" do?

Remove a product from the shopping cart of this browser on Alternate Germany (alternate.de, the German store), from its Alternate product id (Art.-Nr.) or product page link, whatever its quantity, as the cart page's delete button does. Returns removed and the cart after it: each line with its product id, name, quantity, unit price and line price in euros (VAT included), the item count, the items total and the currency. A product that is not in the cart gives removed false and the cart unchanged, not an error. Works as a guest, with no account.

### How do I automatically remove a product from the Alternate cart on alternate.de?

Ask an AI agent connected to Reduck to run reduck/alternate.de/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/alternate.de/remove_from_cart

### Is there a alternate.de API to remove a product from the Alternate cart?

You do not need one. "Remove a product from the Alternate cart" drives the real alternate.de pages in a browser, so it works whether or not alternate.de offers an API for this.

### What information do I need to provide?

Required: product.

### What does it return?

It returns count, lines, total, removed, currency.

### Do I need to be logged in to alternate.de?

No. It only uses pages of alternate.de that are reachable without signing in.

### Does it change anything on alternate.de, or only read data?

It makes changes on alternate.de, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/alternate.de/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/alternate.de/remove_from_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/alternate.de/remove_from_cart
