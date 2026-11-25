# Add to Coolblue cart

Automatically add to Coolblue cart on coolblue.nl. Add a Coolblue Netherlands (coolblue.nl) product to the shopping cart from its product number or product link, with an optional quantity from 1 to 10, and return the cart as the site holds it afterwards: each line with its line id, product number, name, quantity, unit price and line price in euros, plus the item count and total. Works as a guest, with no account: the cart lives in the browser, so lines already in it stay and are listed too. Nothing is paid or ordered. A product that has no add button (out of stock, sold in store only) fails with an error; a link that is not a Coolblue product page, or an unknown product number, fails with an error.

- Site: coolblue.nl
- Address: `reduck/coolblue.nl/add_to_cart`
- Updated: 2026-11-24 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/coolblue.nl/add_to_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/coolblue.nl/add_to_cart
```

## Input

- `product` (string, required): Coolblue product number (the product_id of Search Coolblue products) or a product link.
- `quantity` (integer, optional): How many to add, 1 to 10.

## Output

- `name` (string | null, required)
- `added` (boolean, required): True when the cart holds the product after the add.
- `count` (integer, required): Number of items in the cart (quantities added up).
- `lines` (array, required)
- `total` (number | null, required): Cart total in euros, VAT included, added up from the lines.
- `offerId` (string | null, required)
- `productId` (string, required): Coolblue product number that was added.

## FAQ

### What does "Add to Coolblue cart" do?

Add a Coolblue Netherlands (coolblue.nl) product to the shopping cart from its product number or product link, with an optional quantity from 1 to 10, and return the cart as the site holds it afterwards: each line with its line id, product number, name, quantity, unit price and line price in euros, plus the item count and total. Works as a guest, with no account: the cart lives in the browser, so lines already in it stay and are listed too. Nothing is paid or ordered. A product that has no add button (out of stock, sold in store only) fails with an error; a link that is not a Coolblue product page, or an unknown product number, fails with an error.

### How do I automatically add to Coolblue cart on coolblue.nl?

Ask an AI agent connected to Reduck to run reduck/coolblue.nl/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/coolblue.nl/add_to_cart

### Is there a coolblue.nl API to add to Coolblue cart?

You do not need one. "Add to Coolblue cart" drives the real coolblue.nl pages in a browser, so it works whether or not coolblue.nl offers an API for this.

### What information do I need to provide?

Required: product. Optional: quantity.

### What does it return?

It returns name, added, count, lines, total, offerId, productId.

### Do I need to be logged in to coolblue.nl?

No. It only uses pages of coolblue.nl that are reachable without signing in.

### Does it change anything on coolblue.nl, or only read data?

It makes changes on coolblue.nl, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/coolblue.nl/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/coolblue.nl/add_to_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/coolblue.nl/add_to_cart
