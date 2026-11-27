# Add a product to the Picard cart

Automatically add a product to the Picard cart on picard.fr. Add a product of the Picard France store (picard.fr, frozen food) to the cart of this browser, from its product id or link, with a quantity from 1 to 99, and return the cart afterwards: each line with its line id, product id, name, seller (always Picard), quantity, unit price and line price in euros, plus the item count and the total of the products. Works as a guest, with no account: when the site asks for a delivery postcode or a store, the script chooses to set it later, so the cart keeps the national prices of the French web store. Lines already in the cart stay and are listed too. Nothing is paid or ordered. An unknown product, a link that is not a Picard product page, a quantity out of range, and a product that the site does not sell online now fail with a message that says so.

- Site: picard.fr
- Address: `reduck/picard.fr/add_to_cart`
- Updated: 2026-11-26 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/picard.fr/add_to_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/picard.fr/add_to_cart
```

## Input

- `product` (string, required): The product id from Search Picard products (for example "000000000000083390") or a picard.fr product link.
- `quantity` (integer, optional): How many units to add, from 1 to 99.

## Output

- `name` (string | null, required)
- `added` (integer, required): Units this run added to the cart.
- `count` (integer, required): Units in the cart after the add.
- `lines` (array, required)
- `total` (number | null, required): Total of the products in euros after the add, delivery and loyalty discounts not included.
- `offerId` (string | null, required): Always null: Picard sells only its own products.
- `currency` (string, required)
- `productId` (string, required)

## FAQ

### What does "Add a product to the Picard cart" do?

Add a product of the Picard France store (picard.fr, frozen food) to the cart of this browser, from its product id or link, with a quantity from 1 to 99, and return the cart afterwards: each line with its line id, product id, name, seller (always Picard), quantity, unit price and line price in euros, plus the item count and the total of the products. Works as a guest, with no account: when the site asks for a delivery postcode or a store, the script chooses to set it later, so the cart keeps the national prices of the French web store. Lines already in the cart stay and are listed too. Nothing is paid or ordered. An unknown product, a link that is not a Picard product page, a quantity out of range, and a product that the site does not sell online now fail with a message that says so.

### How do I automatically add a product to the Picard cart on picard.fr?

Ask an AI agent connected to Reduck to run reduck/picard.fr/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/picard.fr/add_to_cart

### Is there a picard.fr API to add a product to the Picard cart?

You do not need one. "Add a product to the Picard cart" drives the real picard.fr pages in a browser, so it works whether or not picard.fr offers an API for this.

### What information do I need to provide?

Required: product. Optional: quantity.

### What does it return?

It returns name, added, count, lines, total, offerId, currency, productId.

### Do I need to be logged in to picard.fr?

No. It only uses pages of picard.fr that are reachable without signing in.

### Does it change anything on picard.fr, or only read data?

It makes changes on picard.fr, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/picard.fr/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/picard.fr/add_to_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/picard.fr/add_to_cart
