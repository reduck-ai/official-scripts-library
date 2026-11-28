# Add a product to the Hot Topic cart

Automatically add a product to the Hot Topic cart on hottopic.com. Add a Hot Topic (hottopic.com, US) product to the shopping bag of this browser, for shipping, and return the bag as the site holds it afterwards. Give the product id or link and, for a product that comes in sizes or colors, the offerId of one of them (both from Get Hot Topic product), with a quantity from 1 to 5. Returns the product id, offer id, name, whether the line is now in the bag, and the bag: the number of units, the estimated subtotal before shipping and tax, and each line with its line id, product id, offer id, name, seller, quantity, unit price and line price in US dollars. Works as a guest, with no account: lines already in the bag stay and are listed too. Nothing is paid or ordered. An unknown product, an offer of another product, a missing offerId, an offer that cannot be shipped now, or a quantity above the limit of the product fails with a message that says so, and adds nothing.

- Site: hottopic.com
- Address: `reduck/hottopic.com/add_to_cart`
- Updated: 2026-11-27 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/hottopic.com/add_to_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/hottopic.com/add_to_cart
```

## Input

- `product` (string, required): Product id (the number at the end of a product link, for example 36930976) or the product link.
- `offerId` (string, optional): Id of the size or color to add, from the variants of Get Hot Topic product. Needed when the product comes in sizes or colors.
- `quantity` (integer, optional): How many to add.

## Output

- `name` (string | null, required)
- `added` (boolean, required): True when the bag now holds a line of this offer.
- `count` (integer, required): Number of units in the bag.
- `lines` (array, required)
- `total` (number | null, required): Estimated subtotal in US dollars, before shipping and tax.
- `offerId` (string, required): Id of the size or color added.
- `productId` (string, required)

## FAQ

### What does "Add a product to the Hot Topic cart" do?

Add a Hot Topic (hottopic.com, US) product to the shopping bag of this browser, for shipping, and return the bag as the site holds it afterwards. Give the product id or link and, for a product that comes in sizes or colors, the offerId of one of them (both from Get Hot Topic product), with a quantity from 1 to 5. Returns the product id, offer id, name, whether the line is now in the bag, and the bag: the number of units, the estimated subtotal before shipping and tax, and each line with its line id, product id, offer id, name, seller, quantity, unit price and line price in US dollars. Works as a guest, with no account: lines already in the bag stay and are listed too. Nothing is paid or ordered. An unknown product, an offer of another product, a missing offerId, an offer that cannot be shipped now, or a quantity above the limit of the product fails with a message that says so, and adds nothing.

### How do I automatically add a product to the Hot Topic cart on hottopic.com?

Ask an AI agent connected to Reduck to run reduck/hottopic.com/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/hottopic.com/add_to_cart

### Is there a hottopic.com API to add a product to the Hot Topic cart?

You do not need one. "Add a product to the Hot Topic cart" drives the real hottopic.com pages in a browser, so it works whether or not hottopic.com offers an API for this.

### What information do I need to provide?

Required: product. Optional: offerId, quantity.

### What does it return?

It returns name, added, count, lines, total, offerId, productId.

### Do I need to be logged in to hottopic.com?

No. It only uses pages of hottopic.com that are reachable without signing in.

### Does it change anything on hottopic.com, or only read data?

It makes changes on hottopic.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/hottopic.com/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/hottopic.com/add_to_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/hottopic.com/add_to_cart
