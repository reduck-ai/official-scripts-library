# Add BUT.fr product to cart

Automatically add BUT.fr product to cart on but.fr. Add a BUT.fr product to the shopping cart from its product page link or product id, with an optional quantity, and return the cart as the site holds it afterwards: each line with its product id, name, seller, quantity, unit price and line price in euros, plus the item count and total. Works as a guest, with no account: the cart lives in the browser, so lines already in it stay and are listed too. Nothing is paid or ordered. A link that is not a BUT product page, or an unknown product, fails with an error; a product that cannot be bought online fails with an error.

- Site: but.fr
- Address: `reduck/but.fr/add_to_cart`
- Updated: 2026-11-24 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/but.fr/add_to_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/but.fr/add_to_cart
```

## Input

- `product` (string, required): Link of a BUT.fr product page (for example https://www.but.fr/produits/4894223246194/Table-basse-noire-INES-Noir.html) or its product id (4894223246194), as Search BUT products gives it.
- `quantity` (integer, optional): How many units to add to the cart.

## Output

- `name` (string | null, required)
- `added` (integer, required): Units this run added to the cart.
- `count` (integer, required): Units in the cart after the add.
- `lines` (array, required)
- `total` (number | null, required): Cart total in euros, taxes included.
- `offerId` (string | null, required)
- `productId` (string, required)

## FAQ

### What does "Add BUT.fr product to cart" do?

Add a BUT.fr product to the shopping cart from its product page link or product id, with an optional quantity, and return the cart as the site holds it afterwards: each line with its product id, name, seller, quantity, unit price and line price in euros, plus the item count and total. Works as a guest, with no account: the cart lives in the browser, so lines already in it stay and are listed too. Nothing is paid or ordered. A link that is not a BUT product page, or an unknown product, fails with an error; a product that cannot be bought online fails with an error.

### How do I automatically add BUT.fr product to cart on but.fr?

Ask an AI agent connected to Reduck to run reduck/but.fr/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/but.fr/add_to_cart

### Is there a but.fr API to add BUT.fr product to cart?

You do not need one. "Add BUT.fr product to cart" drives the real but.fr pages in a browser, so it works whether or not but.fr offers an API for this.

### What information do I need to provide?

Required: product. Optional: quantity.

### What does it return?

It returns name, added, count, lines, total, offerId, productId.

### Do I need to be logged in to but.fr?

No. It only uses pages of but.fr that are reachable without signing in.

### Does it change anything on but.fr, or only read data?

It makes changes on but.fr, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/but.fr/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/but.fr/add_to_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/but.fr/add_to_cart
