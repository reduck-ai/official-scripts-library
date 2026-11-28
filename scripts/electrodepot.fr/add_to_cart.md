# Add Electro Dépôt product to cart

Automatically add Electro Dépôt product to cart on electrodepot.fr. Add a product of the Electro Dépôt French store (electrodepot.fr) to the shopping cart of this browser, from its product id or product page link, with a quantity from 1 to 10, as the product page's add to cart button does. Returns the cart as the site holds it afterwards, in the shape List Electro Dépôt cart items gives (item count, items total in euros, currency, lines), plus the product id, offer id (always null), name and the units added. Works as a guest, with no account: lines already in the cart stay. A product id or link the site does not know, and a product the site refuses to add, fail with an error that says so. Nothing is paid or ordered.

- Site: electrodepot.fr
- Address: `reduck/electrodepot.fr/add_to_cart`
- Updated: 2026-11-27 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/electrodepot.fr/add_to_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/electrodepot.fr/add_to_cart
```

## Input

- `product` (string, required): Product id from Search Electro Dépôt products (for example 36453), or a product page link such as https://www.electrodepot.fr/casque-bluetooth-edenwood-supra-b01.html.
- `quantity` (integer, optional): How many units to add.

## Output

- `name` (string | null, required)
- `added` (integer, required): Units this run added.
- `count` (integer, required): Units in the cart.
- `lines` (array, required)
- `total` (number, required): Items total in euros, taxes included, delivery not included.
- `offerId` (string | null, required)
- `currency` (string, required)
- `productId` (string, required)

## FAQ

### What does "Add Electro Dépôt product to cart" do?

Add a product of the Electro Dépôt French store (electrodepot.fr) to the shopping cart of this browser, from its product id or product page link, with a quantity from 1 to 10, as the product page's add to cart button does. Returns the cart as the site holds it afterwards, in the shape List Electro Dépôt cart items gives (item count, items total in euros, currency, lines), plus the product id, offer id (always null), name and the units added. Works as a guest, with no account: lines already in the cart stay. A product id or link the site does not know, and a product the site refuses to add, fail with an error that says so. Nothing is paid or ordered.

### How do I automatically add Electro Dépôt product to cart on electrodepot.fr?

Ask an AI agent connected to Reduck to run reduck/electrodepot.fr/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/electrodepot.fr/add_to_cart

### Is there a electrodepot.fr API to add Electro Dépôt product to cart?

You do not need one. "Add Electro Dépôt product to cart" drives the real electrodepot.fr pages in a browser, so it works whether or not electrodepot.fr offers an API for this.

### What information do I need to provide?

Required: product. Optional: quantity.

### What does it return?

It returns name, added, count, lines, total, offerId, currency, productId.

### Do I need to be logged in to electrodepot.fr?

No. It only uses pages of electrodepot.fr that are reachable without signing in.

### Does it change anything on electrodepot.fr, or only read data?

It makes changes on electrodepot.fr, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/electrodepot.fr/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/electrodepot.fr/add_to_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/electrodepot.fr/add_to_cart
