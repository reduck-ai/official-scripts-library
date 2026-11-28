# Add a product to the Alternate cart

Automatically add a product to the Alternate cart on alternate.de. Add a product of Alternate Germany (alternate.de, the German store) to the shopping cart of this browser, from its Alternate product id (Art.-Nr.) or product page link, with a quantity, as the product page's add button does. Returns the product id and name, the units added, and the cart after the add: each line with its product id, name, quantity, unit price and line price in euros (VAT included), the item count, the items total and the currency. Alternate sells every product itself, so offerId and seller are null. Works as a guest, with no account: lines already in the cart stay. Nothing is ordered or paid. An unknown product, or a product page with no add button, fails with an error that says so.

- Site: alternate.de
- Address: `reduck/alternate.de/add_to_cart`
- Updated: 2026-11-27 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/alternate.de/add_to_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/alternate.de/add_to_cart
```

## Input

- `product` (string, required): An Alternate product id (Art.-Nr.) as Search Alternate products returns it, for example 1864243, or an alternate.de product page link.
- `quantity` (integer, optional): How many units to add.

## Output

- `name` (string | null, required)
- `added` (integer, required): Units this run added.
- `count` (integer, required): Units in the cart after the add.
- `lines` (array, required)
- `total` (number | null, required): Total of the item lines in euros, VAT included, delivery not included.
- `offerId` (string | null, required): Always null: Alternate has one offer per product.
- `currency` (string, required)
- `productId` (string, required)

## FAQ

### What does "Add a product to the Alternate cart" do?

Add a product of Alternate Germany (alternate.de, the German store) to the shopping cart of this browser, from its Alternate product id (Art.-Nr.) or product page link, with a quantity, as the product page's add button does. Returns the product id and name, the units added, and the cart after the add: each line with its product id, name, quantity, unit price and line price in euros (VAT included), the item count, the items total and the currency. Alternate sells every product itself, so offerId and seller are null. Works as a guest, with no account: lines already in the cart stay. Nothing is ordered or paid. An unknown product, or a product page with no add button, fails with an error that says so.

### How do I automatically add a product to the Alternate cart on alternate.de?

Ask an AI agent connected to Reduck to run reduck/alternate.de/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/alternate.de/add_to_cart

### Is there a alternate.de API to add a product to the Alternate cart?

You do not need one. "Add a product to the Alternate cart" drives the real alternate.de pages in a browser, so it works whether or not alternate.de offers an API for this.

### What information do I need to provide?

Required: product. Optional: quantity.

### What does it return?

It returns name, added, count, lines, total, offerId, currency, productId.

### Do I need to be logged in to alternate.de?

No. It only uses pages of alternate.de that are reachable without signing in.

### Does it change anything on alternate.de, or only read data?

It makes changes on alternate.de, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/alternate.de/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/alternate.de/add_to_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/alternate.de/add_to_cart
