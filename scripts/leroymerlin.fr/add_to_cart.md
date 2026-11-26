# Add Leroy Merlin product to cart

Automatically add Leroy Merlin product to cart on leroymerlin.fr. Add a Leroy Merlin product to the shopping cart from its product page link, with an optional quantity, and return the cart as the site holds it afterwards: each line with its product reference, offer id, name, seller, quantity, unit price and line price in euros, plus the item count and the items total. Works as a guest, with no account: the cart lives in the browser, so lines already in it stay and are listed too. Nothing is paid or ordered. A product page that does not offer the add button (out of stock, not sold online) fails with an error; a link that is not a Leroy Merlin product page fails with an error.

- Site: leroymerlin.fr
- Address: `reduck/leroymerlin.fr/add_to_cart`
- Updated: 2026-11-24 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/leroymerlin.fr/add_to_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/leroymerlin.fr/add_to_cart
```

## Input

- `url` (string, required): Link of a Leroy Merlin product page, as in https://www.leroymerlin.fr/produits/vis-acier-tete-fraisee-pozidriv-standers-4-x-l-50-mm-82231854.html.
- `quantity` (integer, optional): How many units to add to the cart.

## Output

- `name` (string | null, required)
- `added` (integer, required): Units this run added to the cart.
- `count` (integer, required): Units in the cart after the add.
- `lines` (array, required)
- `total` (number | null, required): Items total in euros, taxes included, delivery excluded.
- `offerId` (string | null, required)
- `productId` (string, required)

## FAQ

### What does "Add Leroy Merlin product to cart" do?

Add a Leroy Merlin product to the shopping cart from its product page link, with an optional quantity, and return the cart as the site holds it afterwards: each line with its product reference, offer id, name, seller, quantity, unit price and line price in euros, plus the item count and the items total. Works as a guest, with no account: the cart lives in the browser, so lines already in it stay and are listed too. Nothing is paid or ordered. A product page that does not offer the add button (out of stock, not sold online) fails with an error; a link that is not a Leroy Merlin product page fails with an error.

### How do I automatically add Leroy Merlin product to cart on leroymerlin.fr?

Ask an AI agent connected to Reduck to run reduck/leroymerlin.fr/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/leroymerlin.fr/add_to_cart

### Is there a leroymerlin.fr API to add Leroy Merlin product to cart?

You do not need one. "Add Leroy Merlin product to cart" drives the real leroymerlin.fr pages in a browser, so it works whether or not leroymerlin.fr offers an API for this.

### What information do I need to provide?

Required: url. Optional: quantity.

### What does it return?

It returns name, added, count, lines, total, offerId, productId.

### Do I need to be logged in to leroymerlin.fr?

No. It only uses pages of leroymerlin.fr that are reachable without signing in.

### Does it change anything on leroymerlin.fr, or only read data?

It makes changes on leroymerlin.fr, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/leroymerlin.fr/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/leroymerlin.fr/add_to_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/leroymerlin.fr/add_to_cart
