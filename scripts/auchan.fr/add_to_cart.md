# Add a product to the Auchan cart

Automatically add a product to the Auchan cart on auchan.fr. Add a product of the Auchan France store (auchan.fr) to the cart of this browser, from its product id, reference or link, with a quantity from 1 to 99, and return the cart afterwards: each line with its line id, product id, offer id, name, seller, quantity, unit price and line price in euros, plus the item count and the cart total. Works as a guest, with no account; lines already in the cart stay and are listed too. Grocery products need a store: pass a postcode and the script chooses the nearest drive or Click & Collect store Auchan lists for it, or keep the store this browser chose before. For a product that marketplace sellers sell, pass the offer id from Get Auchan product offers to buy from that seller; without it, the offer the site shows first is added. Nothing is paid or ordered, and no delivery slot is booked. An unknown product, a link that is not an Auchan product page, a quantity out of range, an offer the product does not have, and a product the site does not sell now fail with a message that says so.

- Site: auchan.fr
- Address: `reduck/auchan.fr/add_to_cart`
- Updated: 2026-11-26 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/auchan.fr/add_to_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/auchan.fr/add_to_cart
```

## Input

- `product` (string, required): The product id or reference from Search Auchan products, or an auchan.fr product link.
- `offerId` (string, optional): The offer id from Get Auchan product offers, to buy from that seller.
- `postcode` (string, optional): French postcode (5 digits). When given, the script chooses the nearest drive or Click & Collect store Auchan lists for it before the add.
- `quantity` (integer, optional): How many units to add, from 1 to 99.

## Output

- `name` (string | null, required)
- `added` (integer, required): Units this run added to the cart.
- `count` (integer, required): Units in the cart after the add.
- `lines` (array, required)
- `total` (number | null, required): Cart total in euros after the add.
- `seller` (string | null, required)
- `offerId` (string | null, required)
- `currency` (string, required)
- `productId` (string, required)

## FAQ

### What does "Add a product to the Auchan cart" do?

Add a product of the Auchan France store (auchan.fr) to the cart of this browser, from its product id, reference or link, with a quantity from 1 to 99, and return the cart afterwards: each line with its line id, product id, offer id, name, seller, quantity, unit price and line price in euros, plus the item count and the cart total. Works as a guest, with no account; lines already in the cart stay and are listed too. Grocery products need a store: pass a postcode and the script chooses the nearest drive or Click & Collect store Auchan lists for it, or keep the store this browser chose before. For a product that marketplace sellers sell, pass the offer id from Get Auchan product offers to buy from that seller; without it, the offer the site shows first is added. Nothing is paid or ordered, and no delivery slot is booked. An unknown product, a link that is not an Auchan product page, a quantity out of range, an offer the product does not have, and a product the site does not sell now fail with a message that says so.

### How do I automatically add a product to the Auchan cart on auchan.fr?

Ask an AI agent connected to Reduck to run reduck/auchan.fr/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/auchan.fr/add_to_cart

### Is there a auchan.fr API to add a product to the Auchan cart?

You do not need one. "Add a product to the Auchan cart" drives the real auchan.fr pages in a browser, so it works whether or not auchan.fr offers an API for this.

### What information do I need to provide?

Required: product. Optional: offerId, postcode, quantity.

### What does it return?

It returns name, added, count, lines, total, seller, offerId, currency, productId.

### Do I need to be logged in to auchan.fr?

No. It only uses pages of auchan.fr that are reachable without signing in.

### Does it change anything on auchan.fr, or only read data?

It makes changes on auchan.fr, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/auchan.fr/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/auchan.fr/add_to_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/auchan.fr/add_to_cart
