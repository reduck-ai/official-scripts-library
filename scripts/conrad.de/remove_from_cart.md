# Remove a product from the Conrad cart

Automatically remove a product from the Conrad cart on conrad.de. Remove a product from the shopping cart of this browser on Conrad Germany (conrad.de, the German store), from its Conrad product id (Bestell-Nr.) or product page link, whatever its quantity, as the cart page's delete button does. When the product is in the cart from several sellers, every line of it is removed, or only the line of the offer id you pass. Returns removed and the cart after it: each line with its line id, product id, offer id, name, seller, quantity, unit price and line price, the item count, the items total, the currency (euros) and whether the prices include VAT. A product that is not in the cart gives removed false and the cart unchanged, not an error. Works as a guest, with no account.

- Site: conrad.de
- Address: `reduck/conrad.de/remove_from_cart`
- Updated: 2026-11-27 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/conrad.de/remove_from_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/conrad.de/remove_from_cart
```

## Input

- `product` (string, required): A Conrad product id (Bestell-Nr.) as List Conrad cart items returns it, for example 3164696, or a conrad.de product page link.
- `offerId` (string, optional): Remove only the line of this offer (from List Conrad cart items). Leave it out to remove every line of the product.

## Output

- `count` (integer, required): Units in the cart after the removal.
- `lines` (array, required)
- `total` (number | null, required): Total of the items in the cart, delivery not included.
- `removed` (boolean, required): True when this run removed a line, false when the product was not in the cart.
- `currency` (string | null, required)
- `pricesIncludeVat` (boolean | null, required)

## FAQ

### What does "Remove a product from the Conrad cart" do?

Remove a product from the shopping cart of this browser on Conrad Germany (conrad.de, the German store), from its Conrad product id (Bestell-Nr.) or product page link, whatever its quantity, as the cart page's delete button does. When the product is in the cart from several sellers, every line of it is removed, or only the line of the offer id you pass. Returns removed and the cart after it: each line with its line id, product id, offer id, name, seller, quantity, unit price and line price, the item count, the items total, the currency (euros) and whether the prices include VAT. A product that is not in the cart gives removed false and the cart unchanged, not an error. Works as a guest, with no account.

### How do I automatically remove a product from the Conrad cart on conrad.de?

Ask an AI agent connected to Reduck to run reduck/conrad.de/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/conrad.de/remove_from_cart

### Is there a conrad.de API to remove a product from the Conrad cart?

You do not need one. "Remove a product from the Conrad cart" drives the real conrad.de pages in a browser, so it works whether or not conrad.de offers an API for this.

### What information do I need to provide?

Required: product. Optional: offerId.

### What does it return?

It returns count, lines, total, removed, currency, pricesIncludeVat.

### Do I need to be logged in to conrad.de?

No. It only uses pages of conrad.de that are reachable without signing in.

### Does it change anything on conrad.de, or only read data?

It makes changes on conrad.de, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/conrad.de/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/conrad.de/remove_from_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/conrad.de/remove_from_cart
