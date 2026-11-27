# Add to Container Store cart

Automatically add to Container Store cart on containerstore.com. Add a product of The Container Store (containerstore.com, US) to the cart of this browser, by product id or link, optionally one of its variants (a color or size, by its SKU id from Get Container Store product), in a quantity of 1 to 20. Without a variant it adds the variant the product page selects. Returns the cart after the add. It does not check out.

- Site: containerstore.com
- Address: `reduck/containerstore.com/add_to_cart`
- Updated: 2026-11-26 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/containerstore.com/add_to_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/containerstore.com/add_to_cart
```

## Input

- `product` (string, required): Product id (the productId in a product link, for example 10022942) or the product link.
- `variant` (string, optional): Optional. Variant (SKU) id of the product, from the variants of Get Container Store product.
- `quantity` (integer, optional): How many to add.

## Output

- `name` (string | null, required)
- `added` (boolean, required)
- `count` (integer, required): Number of units in the cart.
- `lines` (array, required)
- `total` (number | null, required): Order subtotal in USD as the cart shows it: before offers, shipping and tax.
- `offerId` (string | null, required): Variant (SKU) id added.
- `productId` (string, required)

## FAQ

### What does "Add to Container Store cart" do?

Add a product of The Container Store (containerstore.com, US) to the cart of this browser, by product id or link, optionally one of its variants (a color or size, by its SKU id from Get Container Store product), in a quantity of 1 to 20. Without a variant it adds the variant the product page selects. Returns the cart after the add. It does not check out.

### How do I automatically add to Container Store cart on containerstore.com?

Ask an AI agent connected to Reduck to run reduck/containerstore.com/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/containerstore.com/add_to_cart

### Is there a containerstore.com API to add to Container Store cart?

You do not need one. "Add to Container Store cart" drives the real containerstore.com pages in a browser, so it works whether or not containerstore.com offers an API for this.

### What information do I need to provide?

Required: product. Optional: variant, quantity.

### What does it return?

It returns name, added, count, lines, total, offerId, productId.

### Do I need to be logged in to containerstore.com?

No. It only uses pages of containerstore.com that are reachable without signing in.

### Does it change anything on containerstore.com, or only read data?

It makes changes on containerstore.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/containerstore.com/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/containerstore.com/add_to_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/containerstore.com/add_to_cart
