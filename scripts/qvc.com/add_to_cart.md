# Add a product to the QVC cart

Automatically add a product to the QVC cart on qvc.com. Add a QVC product to the cart and return the cart.

- Site: qvc.com
- Address: `reduck/qvc.com/add_to_cart`
- Updated: 2026-11-25 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/qvc.com/add_to_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/qvc.com/add_to_cart
```

## Input

- `product` (string, required): QVC item number (e.g. K316571) or a QVC product page link.
- `variant` (string, optional): Variant id from get-product (e.g. A738737-CY7-T15). Needed when the product has more than one color or size available.
- `quantity` (integer, optional)

## Output

- `name` (string | null, required)
- `added` (boolean, required)
- `count` (integer, required): Number of units in the cart.
- `lines` (array, required)
- `total` (number | null, required): Merchandise subtotal in USD, without tax and shipping.
- `offerId` (string | null, required): Variant id that was added.
- `productId` (string, required)

## FAQ

### What does "Add a product to the QVC cart" do?

Add a QVC product to the cart and return the cart.

### How do I automatically add a product to the QVC cart on qvc.com?

Ask an AI agent connected to Reduck to run reduck/qvc.com/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/qvc.com/add_to_cart

### Is there a qvc.com API to add a product to the QVC cart?

You do not need one. "Add a product to the QVC cart" drives the real qvc.com pages in a browser, so it works whether or not qvc.com offers an API for this.

### What information do I need to provide?

Required: product. Optional: variant, quantity.

### What does it return?

It returns name, added, count, lines, total, offerId, productId.

### Do I need to be logged in to qvc.com?

No. It only uses pages of qvc.com that are reachable without signing in.

### Does it change anything on qvc.com, or only read data?

It makes changes on qvc.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/qvc.com/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/qvc.com/add_to_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/qvc.com/add_to_cart
