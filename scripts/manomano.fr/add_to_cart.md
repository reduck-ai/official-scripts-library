# Add ManoMano product to cart

Automatically add ManoMano product to cart on manomano.fr. Add a ManoMano.fr product to the shopping cart from its product page link, with an optional quantity, and return the cart as the site holds it afterwards: each line with its product id, name, the seller that ships it, quantity, unit price and line price in euros, plus the item count and the total of the products. Works as a guest, with no account: the cart lives in the browser, so lines already in it stay and are listed too. Nothing is paid or ordered. A product page that does not offer the add button (unavailable) fails with an error; a link that is not a ManoMano product page fails with an error.

- Site: manomano.fr
- Address: `reduck/manomano.fr/add_to_cart`
- Updated: 2026-11-24 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/manomano.fr/add_to_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/manomano.fr/add_to_cart
```

## Input

- `url` (string, required): Link of a ManoMano product page, as returned by Search ManoMano products, for example https://www.manomano.fr/p/vis-charpente-...-86361787?product_id=148926815. The product id in the link picks the seller's offer.
- `quantity` (integer, optional): How many units to add to the cart.

## Output

- `name` (string | null, required)
- `added` (integer, required): Units this run added to the cart.
- `count` (integer, required): Units in the cart after the add.
- `lines` (array, required)
- `total` (number | null, required): Total of the products in euros, taxes included, delivery not included.
- `productId` (string, required)
- `offerId` (string | null, optional)

## FAQ

### What does "Add ManoMano product to cart" do?

Add a ManoMano.fr product to the shopping cart from its product page link, with an optional quantity, and return the cart as the site holds it afterwards: each line with its product id, name, the seller that ships it, quantity, unit price and line price in euros, plus the item count and the total of the products. Works as a guest, with no account: the cart lives in the browser, so lines already in it stay and are listed too. Nothing is paid or ordered. A product page that does not offer the add button (unavailable) fails with an error; a link that is not a ManoMano product page fails with an error.

### How do I automatically add ManoMano product to cart on manomano.fr?

Ask an AI agent connected to Reduck to run reduck/manomano.fr/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/manomano.fr/add_to_cart

### Is there a manomano.fr API to add ManoMano product to cart?

You do not need one. "Add ManoMano product to cart" drives the real manomano.fr pages in a browser, so it works whether or not manomano.fr offers an API for this.

### What information do I need to provide?

Required: url. Optional: quantity.

### What does it return?

It returns name, added, count, lines, total, offerId, productId.

### Do I need to be logged in to manomano.fr?

No. It only uses pages of manomano.fr that are reachable without signing in.

### Does it change anything on manomano.fr, or only read data?

It makes changes on manomano.fr, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/manomano.fr/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/manomano.fr/add_to_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/manomano.fr/add_to_cart
