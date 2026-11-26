# Remove a product from the Home Depot cart

Automatically remove a product from the Home Depot cart on homedepot.com. Removes every line of one homedepot.com product (itemId or product link) from this browser's cart, whatever its quantity, and returns the cart after. A product that is not in the cart returns removed false and the unchanged cart.

- Site: homedepot.com
- Address: `reduck/homedepot.com/remove_from_cart`
- Updated: 2026-11-25 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/homedepot.com/remove_from_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/homedepot.com/remove_from_cart
```

## Input

- `product` (string, required): The itemId (productId of a cart line) or a product link.

## Output

- `count` (number, required)
- `lines` (array, required)
- `removed` (boolean, required)
- `productId` (string, required)
- `total` (number | null, optional)

## FAQ

### What does "Remove a product from the Home Depot cart" do?

Removes every line of one homedepot.com product (itemId or product link) from this browser's cart, whatever its quantity, and returns the cart after. A product that is not in the cart returns removed false and the unchanged cart.

### How do I automatically remove a product from the Home Depot cart on homedepot.com?

Ask an AI agent connected to Reduck to run reduck/homedepot.com/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/homedepot.com/remove_from_cart

### Is there a homedepot.com API to remove a product from the Home Depot cart?

You do not need one. "Remove a product from the Home Depot cart" drives the real homedepot.com pages in a browser, so it works whether or not homedepot.com offers an API for this.

### What information do I need to provide?

Required: product.

### What does it return?

It returns count, lines, total, removed, productId.

### Do I need to be logged in to homedepot.com?

No. It only uses pages of homedepot.com that are reachable without signing in.

### Does it change anything on homedepot.com, or only read data?

It makes changes on homedepot.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/homedepot.com/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/homedepot.com/remove_from_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/homedepot.com/remove_from_cart
