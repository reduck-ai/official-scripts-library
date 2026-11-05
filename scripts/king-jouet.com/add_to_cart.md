# Add King Jouet product to cart

Automatically add King Jouet product to cart on king-jouet.com. Add a King Jouet product to the shopping cart from its product page link, with an optional quantity, and return the cart as the site holds it afterwards: each line with its reference, quantity and prices, plus the item count and total. Works as a guest, with no account: the cart lives in the browser, so lines already in it stay and are listed too. Nothing is paid or ordered. A product page that does not offer the web add button (out of stock, store pickup only) fails with the availability the page declares; a link that is not a King Jouet product page fails with an error.

- Site: king-jouet.com
- Address: `reduck/king-jouet.com/add_to_cart`
- Updated: 2026-11-04 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/king-jouet.com/add_to_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/king-jouet.com/add_to_cart
```

## Input

- `url` (string, required): Link of a King Jouet product page, as in https://www.king-jouet.com/jeu-jouet/.../ref-1029224-....htm.
- `quantity` (integer, optional): How many units to add to the cart.

## Output

- `ref` (string, required): King Jouet product reference taken from the link.
- `name` (string | null, required)
- `added` (integer, required): Units this run added to the cart.
- `count` (integer, required): Units in the cart after the add.
- `lines` (array, required)
- `total` (number | null, required): Cart total in euros, taxes included.

## FAQ

### What does "Add King Jouet product to cart" do?

Add a King Jouet product to the shopping cart from its product page link, with an optional quantity, and return the cart as the site holds it afterwards: each line with its reference, quantity and prices, plus the item count and total. Works as a guest, with no account: the cart lives in the browser, so lines already in it stay and are listed too. Nothing is paid or ordered. A product page that does not offer the web add button (out of stock, store pickup only) fails with the availability the page declares; a link that is not a King Jouet product page fails with an error.

### How do I automatically add King Jouet product to cart on king-jouet.com?

Ask an AI agent connected to Reduck to run reduck/king-jouet.com/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/king-jouet.com/add_to_cart

### Is there a king-jouet.com API to add King Jouet product to cart?

You do not need one. "Add King Jouet product to cart" drives the real king-jouet.com pages in a browser, so it works whether or not king-jouet.com offers an API for this.

### What information do I need to provide?

Required: url. Optional: quantity.

### What does it return?

It returns ref, name, added, count, lines, total.

### Do I need to be logged in to king-jouet.com?

No. It only uses pages of king-jouet.com that are reachable without signing in.

### Does it change anything on king-jouet.com, or only read data?

It makes changes on king-jouet.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/king-jouet.com/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/king-jouet.com/add_to_cart

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/king-jouet.com/add_to_cart
