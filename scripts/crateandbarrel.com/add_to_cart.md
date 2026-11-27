# Add to Crate & Barrel cart

Automatically add to Crate & Barrel cart on crateandbarrel.com. Add a Crate & Barrel product (crateandbarrel.com, US) to the cart of this browser, by product id or link, optionally one of its variants (color, size), in a quantity of 1 to 10. Returns the cart after the add. It does not check out.

- Site: crateandbarrel.com
- Address: `reduck/crateandbarrel.com/add_to_cart`
- Updated: 2026-11-26 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/crateandbarrel.com/add_to_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/crateandbarrel.com/add_to_cart
```

## Input

- `product` (string, required): Product id (the number after /s in a product link, for example 216478) or the product link.
- `variant` (string, optional): Optional. Id of one variant of the product (a color or size), from the variants of Get Crate & Barrel product. Each variant is its own product id.
- `quantity` (integer, optional): How many to add.

## Output

- `name` (string | null, required)
- `added` (boolean, required): True when the site added the product to the cart.
- `count` (integer, required): Number of items (units) in the cart after the add.
- `lines` (array, required)
- `total` (number | null, required): Item subtotal in USD, without tax or shipping.
- `offerId` (string | null, required)
- `productId` (string, required): Id of the product added (the variant, when one was given).

## FAQ

### What does "Add to Crate & Barrel cart" do?

Add a Crate & Barrel product (crateandbarrel.com, US) to the cart of this browser, by product id or link, optionally one of its variants (color, size), in a quantity of 1 to 10. Returns the cart after the add. It does not check out.

### How do I automatically add to Crate & Barrel cart on crateandbarrel.com?

Ask an AI agent connected to Reduck to run reduck/crateandbarrel.com/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/crateandbarrel.com/add_to_cart

### Is there a crateandbarrel.com API to add to Crate & Barrel cart?

You do not need one. "Add to Crate & Barrel cart" drives the real crateandbarrel.com pages in a browser, so it works whether or not crateandbarrel.com offers an API for this.

### What information do I need to provide?

Required: product. Optional: variant, quantity.

### What does it return?

It returns name, added, count, lines, total, offerId, productId.

### Do I need to be logged in to crateandbarrel.com?

No. It only uses pages of crateandbarrel.com that are reachable without signing in.

### Does it change anything on crateandbarrel.com, or only read data?

It makes changes on crateandbarrel.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/crateandbarrel.com/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/crateandbarrel.com/add_to_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/crateandbarrel.com/add_to_cart
