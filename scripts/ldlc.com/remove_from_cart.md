# Remove LDLC product from cart

Automatically remove LDLC product from cart on ldlc.com. Remove a product from the LDLC cart of this browser by its product id (PB00630480) or offer id, whatever its quantity, and return what is left in the cart: each line with its product id, offer id, name, quantity, unit price and line price in euros, plus the item count and total. A product that is not in the cart is reported with removed false and the cart unchanged, not as a failure.

- Site: ldlc.com
- Address: `reduck/ldlc.com/remove_from_cart`
- Updated: 2026-11-24 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/ldlc.com/remove_from_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/ldlc.com/remove_from_cart
```

## Input

- `product` (string, required): Product id (PB00630480) or product page link of the line to remove, or the offer id (AR202403060058) as the cart lists it.

## Output

- `count` (integer, required)
- `lines` (array, required)
- `total` (number | null, required)
- `removed` (boolean, required): True when the product was in the cart and is gone.

## FAQ

### What does "Remove LDLC product from cart" do?

Remove a product from the LDLC cart of this browser by its product id (PB00630480) or offer id, whatever its quantity, and return what is left in the cart: each line with its product id, offer id, name, quantity, unit price and line price in euros, plus the item count and total. A product that is not in the cart is reported with removed false and the cart unchanged, not as a failure.

### How do I automatically remove LDLC product from cart on ldlc.com?

Ask an AI agent connected to Reduck to run reduck/ldlc.com/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/ldlc.com/remove_from_cart

### Is there a ldlc.com API to remove LDLC product from cart?

You do not need one. "Remove LDLC product from cart" drives the real ldlc.com pages in a browser, so it works whether or not ldlc.com offers an API for this.

### What information do I need to provide?

Required: product.

### What does it return?

It returns count, lines, total, removed.

### Do I need to be logged in to ldlc.com?

No. It only uses pages of ldlc.com that are reachable without signing in.

### Does it change anything on ldlc.com, or only read data?

It makes changes on ldlc.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/ldlc.com/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/ldlc.com/remove_from_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/ldlc.com/remove_from_cart
