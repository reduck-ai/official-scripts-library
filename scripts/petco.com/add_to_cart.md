# Add a product to the Petco cart

Automatically add a product to the Petco cart on petco.com. Add a Petco (petco.com, US) product to the cart of this browser for shipping, and return the cart as the site holds it afterwards. Give the product id or link and, for a product with several sizes, the offerId (item number) of one size (both from Get Petco product), with a quantity from 1 to 10. Without offerId, the size that the link or item number names, or the one the page selects, is added. Returns the product id, offer id, name, whether the cart now holds the offer, and the cart: the number of units, the subtotal before shipping and tax, and each line with its line id, offer id, name, seller, quantity, unit price and line price in US dollars. Works as a guest, with no account: lines already in the cart stay and are listed too. Nothing is paid or ordered. An unknown product, an offerId of another product, an item that cannot be ordered, or a quantity above the units in stock fails with a message that says so, and adds nothing. Use a managed browser with country US.

- Site: petco.com
- Address: `reduck/petco.com/add_to_cart`
- Updated: 2026-11-27 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/petco.com/add_to_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/petco.com/add_to_cart
```

## Input

- `product` (string, required): Product id (for example 5030043), the item number of one size (for example 2998871) or the product link.
- `offerId` (string, optional): Item number of the size to add, from the variants of Get Petco product. Without it, the size that the product link or number names, or the one the page selects, is added.
- `quantity` (integer, optional): How many to add.

## Output

- `name` (string | null, required)
- `added` (boolean, required): True when the cart now holds a line of this offer.
- `count` (integer, required): Number of units in the cart.
- `lines` (array, required)
- `total` (number | null, required): Subtotal in US dollars, before shipping and tax.
- `offerId` (string, required)
- `productId` (string, required)

## FAQ

### What does "Add a product to the Petco cart" do?

Add a Petco (petco.com, US) product to the cart of this browser for shipping, and return the cart as the site holds it afterwards. Give the product id or link and, for a product with several sizes, the offerId (item number) of one size (both from Get Petco product), with a quantity from 1 to 10. Without offerId, the size that the link or item number names, or the one the page selects, is added. Returns the product id, offer id, name, whether the cart now holds the offer, and the cart: the number of units, the subtotal before shipping and tax, and each line with its line id, offer id, name, seller, quantity, unit price and line price in US dollars. Works as a guest, with no account: lines already in the cart stay and are listed too. Nothing is paid or ordered. An unknown product, an offerId of another product, an item that cannot be ordered, or a quantity above the units in stock fails with a message that says so, and adds nothing. Use a managed browser with country US.

### How do I automatically add a product to the Petco cart on petco.com?

Ask an AI agent connected to Reduck to run reduck/petco.com/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/petco.com/add_to_cart

### Is there a petco.com API to add a product to the Petco cart?

You do not need one. "Add a product to the Petco cart" drives the real petco.com pages in a browser, so it works whether or not petco.com offers an API for this.

### What information do I need to provide?

Required: product. Optional: offerId, quantity.

### What does it return?

It returns name, added, count, lines, total, offerId, productId.

### Do I need to be logged in to petco.com?

No. It only uses pages of petco.com that are reachable without signing in.

### Does it change anything on petco.com, or only read data?

It makes changes on petco.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/petco.com/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/petco.com/add_to_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/petco.com/add_to_cart
