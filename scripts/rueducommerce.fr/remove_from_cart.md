# Remove a product from the Rue du Commerce cart

Automatically remove a product from the Rue du Commerce cart on rueducommerce.fr. Removes a product line (whatever its quantity) from the guest cart of rueducommerce.fr, by product id or offer id, and returns the cart after removal. A product that is not in the cart returns removed false and the cart unchanged.

- Site: rueducommerce.fr
- Address: `reduck/rueducommerce.fr/remove_from_cart`
- Updated: 2026-11-24 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/rueducommerce.fr/remove_from_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/rueducommerce.fr/remove_from_cart
```

## Input

- `product` (string, required): Product id (for example r25109147605) or offer id (for example AR202509260012) of a cart line, as returned by list_cart_items.

## Output

- `count` (integer, required)
- `lines` (array, required)
- `total` (number | null, required)
- `removed` (boolean, required)

## FAQ

### What does "Remove a product from the Rue du Commerce cart" do?

Removes a product line (whatever its quantity) from the guest cart of rueducommerce.fr, by product id or offer id, and returns the cart after removal. A product that is not in the cart returns removed false and the cart unchanged.

### How do I automatically remove a product from the Rue du Commerce cart on rueducommerce.fr?

Ask an AI agent connected to Reduck to run reduck/rueducommerce.fr/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/rueducommerce.fr/remove_from_cart

### Is there a rueducommerce.fr API to remove a product from the Rue du Commerce cart?

You do not need one. "Remove a product from the Rue du Commerce cart" drives the real rueducommerce.fr pages in a browser, so it works whether or not rueducommerce.fr offers an API for this.

### What information do I need to provide?

Required: product.

### What does it return?

It returns count, lines, total, removed.

### Do I need to be logged in to rueducommerce.fr?

No. It only uses pages of rueducommerce.fr that are reachable without signing in.

### Does it change anything on rueducommerce.fr, or only read data?

It makes changes on rueducommerce.fr, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/rueducommerce.fr/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/rueducommerce.fr/remove_from_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/rueducommerce.fr/remove_from_cart
