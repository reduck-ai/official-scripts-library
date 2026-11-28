# Add a product to the Conrad cart

Automatically add a product to the Conrad cart on conrad.de. Add a product of Conrad Germany (conrad.de, the German store) to the shopping cart of this browser, from its Conrad product id (Bestell-Nr.) or product page link, with a quantity, as the product page's add button does. By default it adds the offer in the buy box; pass an offer id from Get Conrad product offers to choose another seller. Returns the product id, the offer id and name added, the units added, and the cart after the add: each line with its line id, product id, offer id, name, seller, quantity, unit price and line price, the item count, the items total, the currency (euros) and whether the prices include VAT. Works as a guest, with no account: lines already in the cart stay. Nothing is ordered or paid. An unknown product, an offer id the product does not have, or an add the site refuses fails with an error that says so.

- Site: conrad.de
- Address: `reduck/conrad.de/add_to_cart`
- Updated: 2026-11-27 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/conrad.de/add_to_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/conrad.de/add_to_cart
```

## Input

- `product` (string, required): A Conrad product id (Bestell-Nr.) as Search Conrad products returns it, for example 3164696, or a conrad.de product page link.
- `offerId` (string, optional): The offer to add, from Get Conrad product offers. Leave it out to add the offer in the buy box.
- `quantity` (integer, optional): How many units to add.

## Output

- `name` (string | null, required)
- `added` (integer, required): Units this run added.
- `count` (integer, required): Units in the cart after the add.
- `lines` (array, required)
- `total` (number | null, required): Total of the items in the cart, delivery not included.
- `offerId` (string, required)
- `currency` (string | null, required)
- `productId` (string, required)
- `pricesIncludeVat` (boolean | null, required)

## FAQ

### What does "Add a product to the Conrad cart" do?

Add a product of Conrad Germany (conrad.de, the German store) to the shopping cart of this browser, from its Conrad product id (Bestell-Nr.) or product page link, with a quantity, as the product page's add button does. By default it adds the offer in the buy box; pass an offer id from Get Conrad product offers to choose another seller. Returns the product id, the offer id and name added, the units added, and the cart after the add: each line with its line id, product id, offer id, name, seller, quantity, unit price and line price, the item count, the items total, the currency (euros) and whether the prices include VAT. Works as a guest, with no account: lines already in the cart stay. Nothing is ordered or paid. An unknown product, an offer id the product does not have, or an add the site refuses fails with an error that says so.

### How do I automatically add a product to the Conrad cart on conrad.de?

Ask an AI agent connected to Reduck to run reduck/conrad.de/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/conrad.de/add_to_cart

### Is there a conrad.de API to add a product to the Conrad cart?

You do not need one. "Add a product to the Conrad cart" drives the real conrad.de pages in a browser, so it works whether or not conrad.de offers an API for this.

### What information do I need to provide?

Required: product. Optional: offerId, quantity.

### What does it return?

It returns name, added, count, lines, total, offerId, currency, productId, pricesIncludeVat.

### Do I need to be logged in to conrad.de?

No. It only uses pages of conrad.de that are reachable without signing in.

### Does it change anything on conrad.de, or only read data?

It makes changes on conrad.de, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/conrad.de/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/conrad.de/add_to_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/conrad.de/add_to_cart
