# Add LDLC product to cart

Automatically add LDLC product to cart on ldlc.com. Add an LDLC product to the shopping cart from its product page link or its product id, with an optional quantity from 1 to 10, and return the cart as the site holds it afterwards: each line with its product id, offer id, name, quantity, unit price and line price in euros, plus the item count and the total. Works as a guest, with no account: the cart lives in the browser, so lines already in it stay and are listed too. Nothing is paid or ordered. A product that is out of stock or not sold online fails with an error; a link that is not an LDLC product page fails with an error.

- Site: ldlc.com
- Address: `reduck/ldlc.com/add_to_cart`
- Updated: 2026-11-24 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/ldlc.com/add_to_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/ldlc.com/add_to_cart
```

## Input

- `product` (string, required): Link of an LDLC product page (https://www.ldlc.com/fiche/PB00630480.html) or its product id (PB00630480), as Search LDLC products returns it.
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

### What does "Add LDLC product to cart" do?

Add an LDLC product to the shopping cart from its product page link or its product id, with an optional quantity from 1 to 10, and return the cart as the site holds it afterwards: each line with its product id, offer id, name, quantity, unit price and line price in euros, plus the item count and the total. Works as a guest, with no account: the cart lives in the browser, so lines already in it stay and are listed too. Nothing is paid or ordered. A product that is out of stock or not sold online fails with an error; a link that is not an LDLC product page fails with an error.

### How do I automatically add LDLC product to cart on ldlc.com?

Ask an AI agent connected to Reduck to run reduck/ldlc.com/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/ldlc.com/add_to_cart

### Is there a ldlc.com API to add LDLC product to cart?

You do not need one. "Add LDLC product to cart" drives the real ldlc.com pages in a browser, so it works whether or not ldlc.com offers an API for this.

### What information do I need to provide?

Required: product. Optional: quantity.

### What does it return?

It returns name, added, count, lines, total, offerId, productId.

### Do I need to be logged in to ldlc.com?

No. It only uses pages of ldlc.com that are reachable without signing in.

### Does it change anything on ldlc.com, or only read data?

It makes changes on ldlc.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/ldlc.com/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/ldlc.com/add_to_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/ldlc.com/add_to_cart
