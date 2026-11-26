# Add a product to the Harbor Freight cart

Automatically add a product to the Harbor Freight cart on harborfreight.com. Add a Harbor Freight product (SKU or product page link) to this browser's guest cart in the given quantity, and return the cart after the add. No store or ZIP code is needed.

- Site: harborfreight.com
- Address: `reduck/harborfreight.com/add_to_cart`
- Updated: 2026-11-25 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/harborfreight.com/add_to_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/harborfreight.com/add_to_cart
```

## Input

- `product` (string, required): The product SKU (for example 70067) or its harborfreight.com product page link.
- `quantity` (integer, optional)

## Output

- `added` (boolean, required)
- `count` (integer, required): Number of units in the cart.
- `lines` (array, required)
- `name` (string | null, optional)
- `total` (number | null, optional): Item subtotal, without tax or shipping.
- `offerId` (string | null, optional)
- `productId` (string | null, optional)

## FAQ

### What does "Add a product to the Harbor Freight cart" do?

Add a Harbor Freight product (SKU or product page link) to this browser's guest cart in the given quantity, and return the cart after the add. No store or ZIP code is needed.

### How do I automatically add a product to the Harbor Freight cart on harborfreight.com?

Ask an AI agent connected to Reduck to run reduck/harborfreight.com/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/harborfreight.com/add_to_cart

### Is there a harborfreight.com API to add a product to the Harbor Freight cart?

You do not need one. "Add a product to the Harbor Freight cart" drives the real harborfreight.com pages in a browser, so it works whether or not harborfreight.com offers an API for this.

### What information do I need to provide?

Required: product. Optional: quantity.

### What does it return?

It returns name, added, count, lines, total, offerId, productId.

### Do I need to be logged in to harborfreight.com?

No. It only uses pages of harborfreight.com that are reachable without signing in.

### Does it change anything on harborfreight.com, or only read data?

It makes changes on harborfreight.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/harborfreight.com/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/harborfreight.com/add_to_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/harborfreight.com/add_to_cart
