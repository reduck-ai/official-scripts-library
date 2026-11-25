# Remove from IKEA France cart

Automatically remove from IKEA France cart on ikea.com. Remove a product from the IKEA France (ikea.com/fr/fr) cart of this browser by its article number, whatever its quantity, and return what is left in the cart: each line with its article number, name, quantity, unit price and line price in euros, plus the item count and total. A product that is not in the cart is reported with removed false and the cart unchanged, not as a failure. Other lines are never touched.

- Site: ikea.com
- Address: `reduck/ikea.com/remove_from_cart`
- Updated: 2026-11-24 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/ikea.com/remove_from_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/ikea.com/remove_from_cart
```

## Input

- `product` (string, required): The 8-digit article number of the line to remove (the productId that List IKEA France cart items returns), or its product page link.

## Output

- `count` (integer, required)
- `lines` (array, required)
- `removed` (boolean, required)
- `productId` (string, required)
- `total` (number | null, optional)

## FAQ

### What does "Remove from IKEA France cart" do?

Remove a product from the IKEA France (ikea.com/fr/fr) cart of this browser by its article number, whatever its quantity, and return what is left in the cart: each line with its article number, name, quantity, unit price and line price in euros, plus the item count and total. A product that is not in the cart is reported with removed false and the cart unchanged, not as a failure. Other lines are never touched.

### How do I automatically remove from IKEA France cart on ikea.com?

Ask an AI agent connected to Reduck to run reduck/ikea.com/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/ikea.com/remove_from_cart

### Is there a ikea.com API to remove from IKEA France cart?

You do not need one. "Remove from IKEA France cart" drives the real ikea.com pages in a browser, so it works whether or not ikea.com offers an API for this.

### What information do I need to provide?

Required: product.

### What does it return?

It returns count, lines, total, removed, productId.

### Do I need to be logged in to ikea.com?

No. It only uses pages of ikea.com that are reachable without signing in.

### Does it change anything on ikea.com, or only read data?

It makes changes on ikea.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/ikea.com/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/ikea.com/remove_from_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/ikea.com/remove_from_cart
