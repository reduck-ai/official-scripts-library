# Add a product to the AutoZone cart

Automatically add a product to the AutoZone cart on autozone.com. Add an AutoZone product to the cart, with the fulfillment the site picks by default (store pickup at the store it chose, or ship-to-home), and return the cart after the add.

- Site: autozone.com
- Address: `reduck/autozone.com/add_to_cart`
- Updated: 2026-11-25 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/autozone.com/add_to_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/autozone.com/add_to_cart
```

## Input

- `product` (string, required): AutoZone product id (e.g. 663640, from search-products) or a product link https://www.autozone.com/p/<name>/<id>.
- `quantity` (integer, optional): How many to add.

## Output

- `name` (string | null, required)
- `added` (boolean, required): True when the cart holds more of this product than before the call.
- `count` (integer, required): Number of items in the cart (sum of quantities).
- `lines` (array, required)
- `total` (number | null, required): Item subtotal in USD, without tax or shipping.
- `offerId` (string | null, required): Always null: AutoZone sells its own stock, with one offer per product.
- `productId` (string | null, required)

## FAQ

### What does "Add a product to the AutoZone cart" do?

Add an AutoZone product to the cart, with the fulfillment the site picks by default (store pickup at the store it chose, or ship-to-home), and return the cart after the add.

### How do I automatically add a product to the AutoZone cart on autozone.com?

Ask an AI agent connected to Reduck to run reduck/autozone.com/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/autozone.com/add_to_cart

### Is there a autozone.com API to add a product to the AutoZone cart?

You do not need one. "Add a product to the AutoZone cart" drives the real autozone.com pages in a browser, so it works whether or not autozone.com offers an API for this.

### What information do I need to provide?

Required: product. Optional: quantity.

### What does it return?

It returns name, added, count, lines, total, offerId, productId.

### Do I need to be logged in to autozone.com?

No. It only uses pages of autozone.com that are reachable without signing in.

### Does it change anything on autozone.com, or only read data?

It makes changes on autozone.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/autozone.com/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/autozone.com/add_to_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/autozone.com/add_to_cart
