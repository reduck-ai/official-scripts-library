# Add to GameStop cart

Automatically add to GameStop cart on gamestop.com. Add a GameStop product (one condition, such as New or Pre-Owned) to the cart of the browser, with a quantity, and return the cart.

- Site: gamestop.com
- Address: `reduck/gamestop.com/add_to_cart`
- Updated: 2026-11-25 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/gamestop.com/add_to_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/gamestop.com/add_to_cart
```

## Input

- `product` (string, required): GameStop product id (for example 425555) or product link.
- `variant` (string, optional): Variant id of the condition to add (New, Pre-Owned, Digital), from get-product variants. Needed only when product is a product with several conditions and no variant chosen.
- `quantity` (integer, optional)

## Output

- `name` (string | null, required)
- `added` (boolean, required)
- `count` (integer, required)
- `lines` (array, required)
- `total` (number | null, required)
- `offerId` (string | null, required): Always null: GameStop sells every product itself, so a product has no separate offers.
- `productId` (string | null, required)

## FAQ

### What does "Add to GameStop cart" do?

Add a GameStop product (one condition, such as New or Pre-Owned) to the cart of the browser, with a quantity, and return the cart.

### How do I automatically add to GameStop cart on gamestop.com?

Ask an AI agent connected to Reduck to run reduck/gamestop.com/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/gamestop.com/add_to_cart

### Is there a gamestop.com API to add to GameStop cart?

You do not need one. "Add to GameStop cart" drives the real gamestop.com pages in a browser, so it works whether or not gamestop.com offers an API for this.

### What information do I need to provide?

Required: product. Optional: variant, quantity.

### What does it return?

It returns name, added, count, lines, total, offerId, productId.

### Do I need to be logged in to gamestop.com?

No. It only uses pages of gamestop.com that are reachable without signing in.

### Does it change anything on gamestop.com, or only read data?

It makes changes on gamestop.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/gamestop.com/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/gamestop.com/add_to_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/gamestop.com/add_to_cart
