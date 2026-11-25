# Add Alza.cz product to cart

Automatically add Alza.cz product to cart on alza.cz. Add an Alza.cz product to the shopping cart from its product page link, with an optional quantity, and return the cart as the site holds it afterwards: each line with its product id, name, quantity, unit price and line price in Czech crowns, plus the item count and total. Works as a guest, with no account: the cart lives in the browser, so lines already in it stay and are listed too. Nothing is paid or ordered. A product page that does not offer the add button (out of stock, sold in store only) fails with an error; a link that is not an Alza product page fails with an error.

- Site: alza.cz
- Address: `reduck/alza.cz/add_to_cart`
- Updated: 2026-11-24 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/alza.cz/add_to_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/alza.cz/add_to_cart
```

## Input

- `url` (string, required): Link of an Alza.cz product page, as Search Alza.cz products gives it, for example https://www.alza.cz/gp-nabijecka-baterii-recyko-b423-4-aa-recyko-2100-mah-d13308667.htm.
- `quantity` (integer, optional): How many units to add to the cart.

## Output

- `name` (string | null, required)
- `added` (integer, required): Units this run added to the cart.
- `count` (integer, required): Units in the cart after the add.
- `lines` (array, required)
- `total` (number | null, required): Cart total in Czech crowns, taxes included.
- `productId` (string, required)

## FAQ

### What does "Add Alza.cz product to cart" do?

Add an Alza.cz product to the shopping cart from its product page link, with an optional quantity, and return the cart as the site holds it afterwards: each line with its product id, name, quantity, unit price and line price in Czech crowns, plus the item count and total. Works as a guest, with no account: the cart lives in the browser, so lines already in it stay and are listed too. Nothing is paid or ordered. A product page that does not offer the add button (out of stock, sold in store only) fails with an error; a link that is not an Alza product page fails with an error.

### How do I automatically add Alza.cz product to cart on alza.cz?

Ask an AI agent connected to Reduck to run reduck/alza.cz/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/alza.cz/add_to_cart

### Is there a alza.cz API to add Alza.cz product to cart?

You do not need one. "Add Alza.cz product to cart" drives the real alza.cz pages in a browser, so it works whether or not alza.cz offers an API for this.

### What information do I need to provide?

Required: url. Optional: quantity.

### What does it return?

It returns name, added, count, lines, total, productId.

### Do I need to be logged in to alza.cz?

No. It only uses pages of alza.cz that are reachable without signing in.

### Does it change anything on alza.cz, or only read data?

It makes changes on alza.cz, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/alza.cz/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/alza.cz/add_to_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/alza.cz/add_to_cart
