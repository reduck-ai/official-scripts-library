# Add a product to the PetSmart cart

Automatically add a product to the PetSmart cart on petsmart.com. Add a PetSmart product to the cart as a one-time purchase.

- Site: petsmart.com
- Address: `reduck/petsmart.com/add_to_cart`
- Updated: 2026-11-25 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/petsmart.com/add_to_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/petsmart.com/add_to_cart
```

## Input

- `product` (string, required): Product id (SKU or master id) or product link.
- `variant` (string, optional): SKU of the size or flavor to add, from get-product variants. Without it, the SKU the product id or link names.
- `quantity` (integer, optional)

## Output

- `added` (boolean, required)
- `count` (integer, required)
- `lines` (array, required)
- `productId` (string | null, required)
- `name` (string | null, optional)
- `total` (number | null, optional): Item subtotal in USD, without tax and shipping.
- `offerId` (string | null, optional)

## FAQ

### What does "Add a product to the PetSmart cart" do?

Add a PetSmart product to the cart as a one-time purchase.

### How do I automatically add a product to the PetSmart cart on petsmart.com?

Ask an AI agent connected to Reduck to run reduck/petsmart.com/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/petsmart.com/add_to_cart

### Is there a petsmart.com API to add a product to the PetSmart cart?

You do not need one. "Add a product to the PetSmart cart" drives the real petsmart.com pages in a browser, so it works whether or not petsmart.com offers an API for this.

### What information do I need to provide?

Required: product. Optional: variant, quantity.

### What does it return?

It returns name, added, count, lines, total, offerId, productId.

### Do I need to be logged in to petsmart.com?

No. It only uses pages of petsmart.com that are reachable without signing in.

### Does it change anything on petsmart.com, or only read data?

It makes changes on petsmart.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/petsmart.com/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/petsmart.com/add_to_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/petsmart.com/add_to_cart
