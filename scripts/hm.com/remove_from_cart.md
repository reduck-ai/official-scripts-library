# Remove H&M France product from cart

Automatically remove H&M France product from cart on hm.com. Remove a product from the H&M France guest cart of this browser (hm.com/fr_fr), whatever its quantity, and return what is left: the item count, the items subtotal in euros and each line with its product id, variant id (offerId), name, seller, quantity, unit price and line price, plus removed. Pass a variant id to remove one size, or a product id or link to remove every size of that product. A product that is not in the cart gives removed false and the cart unchanged, not an error.

- Site: hm.com
- Address: `reduck/hm.com/remove_from_cart`
- Updated: 2026-11-25 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/hm.com/remove_from_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/hm.com/remove_from_cart
```

## Input

- `product` (string, required): Variant id (13 digits) to remove one size, or product id (10 digits) to remove every size of that product. A product link works too.

## Output

- `count` (integer, required)
- `lines` (array, required)
- `total` (number | null, required)
- `removed` (boolean, required)

## FAQ

### What does "Remove H&M France product from cart" do?

Remove a product from the H&M France guest cart of this browser (hm.com/fr_fr), whatever its quantity, and return what is left: the item count, the items subtotal in euros and each line with its product id, variant id (offerId), name, seller, quantity, unit price and line price, plus removed. Pass a variant id to remove one size, or a product id or link to remove every size of that product. A product that is not in the cart gives removed false and the cart unchanged, not an error.

### How do I automatically remove H&M France product from cart on hm.com?

Ask an AI agent connected to Reduck to run reduck/hm.com/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/hm.com/remove_from_cart

### Is there a hm.com API to remove H&M France product from cart?

You do not need one. "Remove H&M France product from cart" drives the real hm.com pages in a browser, so it works whether or not hm.com offers an API for this.

### What information do I need to provide?

Required: product.

### What does it return?

It returns count, lines, total, removed.

### Do I need to be logged in to hm.com?

No. It only uses pages of hm.com that are reachable without signing in.

### Does it change anything on hm.com, or only read data?

It makes changes on hm.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/hm.com/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/hm.com/remove_from_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/hm.com/remove_from_cart
