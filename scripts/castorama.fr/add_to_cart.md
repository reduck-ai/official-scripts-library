# Add Castorama product to cart

Automatically add Castorama product to cart on castorama.fr. Add a castorama.fr product to the shopping cart from its product page link or product id, with an optional quantity, and return the cart as the site holds it afterwards: each line with its product id, offer id, name, seller, quantity, unit price and line price in euros, plus the item count and total. Works as a guest, with no account: the cart lives in the browser, so lines already in it stay and are listed too. Nothing is paid or ordered. A product that cannot be bought online (out of stock, sold in store only) fails with an error; a link that is not a Castorama product page fails with an error.

- Site: castorama.fr
- Address: `reduck/castorama.fr/add_to_cart`
- Updated: 2026-11-24 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/castorama.fr/add_to_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/castorama.fr/add_to_cart
```

## Input

- `product` (string, required): A castorama.fr product link (ends with <id>_CAFR.prd) or the product id returned by Search Castorama products.
- `quantity` (integer, optional): How many units to add to the cart.

## Output

- `name` (string | null, required)
- `added` (integer, required): Units this run added to the cart.
- `count` (integer, required): Units in the cart after the add.
- `lines` (array, required)
- `total` (number | null, required): Cart total in euros, taxes included, delivery not included.
- `offerId` (string | null, required)
- `productId` (string, required)

## FAQ

### What does "Add Castorama product to cart" do?

Add a castorama.fr product to the shopping cart from its product page link or product id, with an optional quantity, and return the cart as the site holds it afterwards: each line with its product id, offer id, name, seller, quantity, unit price and line price in euros, plus the item count and total. Works as a guest, with no account: the cart lives in the browser, so lines already in it stay and are listed too. Nothing is paid or ordered. A product that cannot be bought online (out of stock, sold in store only) fails with an error; a link that is not a Castorama product page fails with an error.

### How do I automatically add Castorama product to cart on castorama.fr?

Ask an AI agent connected to Reduck to run reduck/castorama.fr/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/castorama.fr/add_to_cart

### Is there a castorama.fr API to add Castorama product to cart?

You do not need one. "Add Castorama product to cart" drives the real castorama.fr pages in a browser, so it works whether or not castorama.fr offers an API for this.

### What information do I need to provide?

Required: product. Optional: quantity.

### What does it return?

It returns name, added, count, lines, total, offerId, productId.

### Do I need to be logged in to castorama.fr?

No. It only uses pages of castorama.fr that are reachable without signing in.

### Does it change anything on castorama.fr, or only read data?

It makes changes on castorama.fr, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/castorama.fr/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/castorama.fr/add_to_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/castorama.fr/add_to_cart
