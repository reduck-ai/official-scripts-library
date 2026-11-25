# Add Conforama product to cart

Automatically add Conforama product to cart on conforama.fr. Add a Conforama product to the shopping cart from its product id or product page link, with an optional quantity, and return the cart as the site holds it afterwards: each line with its product id, offer id, name, seller, quantity, unit price and line price in euros, plus the item count and total. Works as a guest, with no account: the cart lives in the browser, so lines already in it stay and are listed too. Nothing is paid or ordered. A product page that does not offer the add button (out of stock, not sold online) fails with an error; a link that is not a Conforama product page fails with an error.

- Site: conforama.fr
- Address: `reduck/conforama.fr/add_to_cart`
- Updated: 2026-11-24 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/conforama.fr/add_to_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/conforama.fr/add_to_cart
```

## Input

- `product` (string, required): Product id such as 769466, or the link of its Conforama product page, as returned by Search Conforama products.
- `quantity` (integer, optional): How many units to add to the cart.

## Output

- `name` (string | null, required)
- `added` (integer, required): Units this run added to the cart.
- `count` (integer, required): Units in the cart after the add.
- `lines` (array, required)
- `total` (number | null, required): Cart total in euros, taxes included.
- `offerId` (string | null, required): Marketplace offer id, null for products sold by Conforama.
- `productId` (string, required)

## FAQ

### What does "Add Conforama product to cart" do?

Add a Conforama product to the shopping cart from its product id or product page link, with an optional quantity, and return the cart as the site holds it afterwards: each line with its product id, offer id, name, seller, quantity, unit price and line price in euros, plus the item count and total. Works as a guest, with no account: the cart lives in the browser, so lines already in it stay and are listed too. Nothing is paid or ordered. A product page that does not offer the add button (out of stock, not sold online) fails with an error; a link that is not a Conforama product page fails with an error.

### How do I automatically add Conforama product to cart on conforama.fr?

Ask an AI agent connected to Reduck to run reduck/conforama.fr/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/conforama.fr/add_to_cart

### Is there a conforama.fr API to add Conforama product to cart?

You do not need one. "Add Conforama product to cart" drives the real conforama.fr pages in a browser, so it works whether or not conforama.fr offers an API for this.

### What information do I need to provide?

Required: product. Optional: quantity.

### What does it return?

It returns name, added, count, lines, total, offerId, productId.

### Do I need to be logged in to conforama.fr?

No. It only uses pages of conforama.fr that are reachable without signing in.

### Does it change anything on conforama.fr, or only read data?

It makes changes on conforama.fr, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/conforama.fr/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/conforama.fr/add_to_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/conforama.fr/add_to_cart
