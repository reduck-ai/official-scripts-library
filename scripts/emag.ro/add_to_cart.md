# Add product to emag.ro cart

Automatically add product to emag.ro cart on emag.ro. Add an emag.ro product to the shopping cart from its product page link or product code, with an optional quantity, and return the cart as the site holds it afterwards: each line with its product id, offer id, name, seller, quantity, unit price and line price in lei (RON), plus the item count and products total. Works as a guest, with no account: the cart lives in the browser, so lines already in it stay and are listed too. Nothing is paid or ordered. A product page that does not offer the add button (out of stock, no longer listed) fails with an error; a link that is not an emag.ro product page fails with an error.

- Site: emag.ro
- Address: `reduck/emag.ro/add_to_cart`
- Updated: 2026-11-24 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/emag.ro/add_to_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/emag.ro/add_to_cart
```

## Input

- `product` (string, required): Link of an emag.ro product page (as Search emag products gives it) or its product code, 9 capital letters and digits, for example DM9NN8MBM.
- `quantity` (integer, optional): How many units to add to the cart.

## Output

- `name` (string | null, required)
- `added` (integer, required): Units this run added to the cart.
- `count` (integer, required): Units in the cart after the add.
- `lines` (array, required)
- `total` (number | null, required): Products total in lei, taxes included.
- `offerId` (string, required)
- `productId` (string, required)

## FAQ

### What does "Add product to emag.ro cart" do?

Add an emag.ro product to the shopping cart from its product page link or product code, with an optional quantity, and return the cart as the site holds it afterwards: each line with its product id, offer id, name, seller, quantity, unit price and line price in lei (RON), plus the item count and products total. Works as a guest, with no account: the cart lives in the browser, so lines already in it stay and are listed too. Nothing is paid or ordered. A product page that does not offer the add button (out of stock, no longer listed) fails with an error; a link that is not an emag.ro product page fails with an error.

### How do I automatically add product to emag.ro cart on emag.ro?

Ask an AI agent connected to Reduck to run reduck/emag.ro/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/emag.ro/add_to_cart

### Is there a emag.ro API to add product to emag.ro cart?

You do not need one. "Add product to emag.ro cart" drives the real emag.ro pages in a browser, so it works whether or not emag.ro offers an API for this.

### What information do I need to provide?

Required: product. Optional: quantity.

### What does it return?

It returns name, added, count, lines, total, offerId, productId.

### Do I need to be logged in to emag.ro?

No. It only uses pages of emag.ro that are reachable without signing in.

### Does it change anything on emag.ro, or only read data?

It makes changes on emag.ro, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/emag.ro/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/emag.ro/add_to_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/emag.ro/add_to_cart
