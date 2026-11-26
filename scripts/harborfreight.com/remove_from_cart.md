# Remove a product from the Harbor Freight cart

Automatically remove a product from the Harbor Freight cart on harborfreight.com. Remove a product (SKU or product page link) from this browser's Harbor Freight guest cart, whatever its quantity, and return the cart. A product that is not in the cart leaves it unchanged.

- Site: harborfreight.com
- Address: `reduck/harborfreight.com/remove_from_cart`
- Updated: 2026-11-25 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/harborfreight.com/remove_from_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/harborfreight.com/remove_from_cart
```

## Input

- `product_id` (string, required): The product SKU (for example 70067) or its harborfreight.com product page link.

## Output

- `count` (integer, required): Number of units in the cart.
- `lines` (array, required)
- `removed` (boolean, required)
- `total` (number | null, optional): Item subtotal, without tax or shipping.

## FAQ

### What does "Remove a product from the Harbor Freight cart" do?

Remove a product (SKU or product page link) from this browser's Harbor Freight guest cart, whatever its quantity, and return the cart. A product that is not in the cart leaves it unchanged.

### How do I automatically remove a product from the Harbor Freight cart on harborfreight.com?

Ask an AI agent connected to Reduck to run reduck/harborfreight.com/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/harborfreight.com/remove_from_cart

### Is there a harborfreight.com API to remove a product from the Harbor Freight cart?

You do not need one. "Remove a product from the Harbor Freight cart" drives the real harborfreight.com pages in a browser, so it works whether or not harborfreight.com offers an API for this.

### What information do I need to provide?

Required: product_id.

### What does it return?

It returns count, lines, total, removed.

### Do I need to be logged in to harborfreight.com?

No. It only uses pages of harborfreight.com that are reachable without signing in.

### Does it change anything on harborfreight.com, or only read data?

It makes changes on harborfreight.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/harborfreight.com/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/harborfreight.com/remove_from_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/harborfreight.com/remove_from_cart
