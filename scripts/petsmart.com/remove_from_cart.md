# Remove a product from the PetSmart cart

Automatically remove a product from the PetSmart cart on petsmart.com. Remove a product from the PetSmart cart, whatever its quantity, and return the cart.

- Site: petsmart.com
- Address: `reduck/petsmart.com/remove_from_cart`
- Updated: 2026-11-25 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/petsmart.com/remove_from_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/petsmart.com/remove_from_cart
```

## Input

- `product_id` (string, required): SKU of the cart line (productId from list_cart_items) or its product link.

## Output

- `count` (integer, required)
- `lines` (array, required)
- `removed` (boolean, required)
- `total` (number | null, optional): Item subtotal in USD, without tax and shipping.

## FAQ

### What does "Remove a product from the PetSmart cart" do?

Remove a product from the PetSmart cart, whatever its quantity, and return the cart.

### How do I automatically remove a product from the PetSmart cart on petsmart.com?

Ask an AI agent connected to Reduck to run reduck/petsmart.com/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/petsmart.com/remove_from_cart

### Is there a petsmart.com API to remove a product from the PetSmart cart?

You do not need one. "Remove a product from the PetSmart cart" drives the real petsmart.com pages in a browser, so it works whether or not petsmart.com offers an API for this.

### What information do I need to provide?

Required: product_id.

### What does it return?

It returns count, lines, total, removed.

### Do I need to be logged in to petsmart.com?

No. It only uses pages of petsmart.com that are reachable without signing in.

### Does it change anything on petsmart.com, or only read data?

It makes changes on petsmart.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/petsmart.com/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/petsmart.com/remove_from_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/petsmart.com/remove_from_cart
