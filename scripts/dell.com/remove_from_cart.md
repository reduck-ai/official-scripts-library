# Remove a product from the Dell cart

Automatically remove a product from the Dell cart on dell.com. Remove every cart line of one product from the Dell US store cart, whatever its quantity, and return the cart. A product that is not in the cart leaves the cart unchanged and returns removed false.

- Site: dell.com
- Address: `reduck/dell.com/remove_from_cart`
- Updated: 2026-11-25 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/dell.com/remove_from_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/dell.com/remove_from_cart
```

## Input

- `product_id` (string, required): Product id as list_cart_items returns it in productId (e.g. "se2426h"), or the link of a Dell US product page.

## Output

- `count` (integer, required)
- `lines` (array, required)
- `total` (number | null, required): Item subtotal after discounts, in USD, without tax and shipping.
- `removed` (boolean, required)

## FAQ

### What does "Remove a product from the Dell cart" do?

Remove every cart line of one product from the Dell US store cart, whatever its quantity, and return the cart. A product that is not in the cart leaves the cart unchanged and returns removed false.

### How do I automatically remove a product from the Dell cart on dell.com?

Ask an AI agent connected to Reduck to run reduck/dell.com/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/dell.com/remove_from_cart

### Is there a dell.com API to remove a product from the Dell cart?

You do not need one. "Remove a product from the Dell cart" drives the real dell.com pages in a browser, so it works whether or not dell.com offers an API for this.

### What information do I need to provide?

Required: product_id.

### What does it return?

It returns count, lines, total, removed.

### Do I need to be logged in to dell.com?

No. It only uses pages of dell.com that are reachable without signing in.

### Does it change anything on dell.com, or only read data?

It makes changes on dell.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/dell.com/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/dell.com/remove_from_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/dell.com/remove_from_cart
