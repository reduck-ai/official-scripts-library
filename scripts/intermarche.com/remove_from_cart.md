# Remove Intermarché product from cart

Automatically remove Intermarché product from cart on intermarche.com. Remove a product from this browser's Intermarché.com cart for one store by barcode number, whatever its quantity, and return the cart left. Takes the line's review_hash from List Intermarché cart items: when it is missing or the line changed since, nothing is removed and the error gives the line as it is now and its hash. A product not in the cart returns removed false. The store is its 5-digit code (for example 09571).

- Site: intermarche.com
- Address: `reduck/intermarche.com/remove_from_cart`
- Updated: 2026-11-26 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/intermarche.com/remove_from_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/intermarche.com/remove_from_cart
```

## Input

- `store` (string, required): Store code, 5 digits, e.g. 09571.
- `product` (string, required): Barcode number as List Intermarché cart items gives it in productId, or the product's intermarche.com/produit/... link.
- `review_hash` (string, optional): review_hash of the line, from List Intermarché cart items.

## Output

- `count` (integer, required)
- `lines` (array, required)
- `total` (number, required)
- `removed` (boolean, required)

## FAQ

### What does "Remove Intermarché product from cart" do?

Remove a product from this browser's Intermarché.com cart for one store by barcode number, whatever its quantity, and return the cart left. Takes the line's review_hash from List Intermarché cart items: when it is missing or the line changed since, nothing is removed and the error gives the line as it is now and its hash. A product not in the cart returns removed false. The store is its 5-digit code (for example 09571).

### How do I automatically remove Intermarché product from cart on intermarche.com?

Ask an AI agent connected to Reduck to run reduck/intermarche.com/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/intermarche.com/remove_from_cart

### Is there a intermarche.com API to remove Intermarché product from cart?

You do not need one. "Remove Intermarché product from cart" drives the real intermarche.com pages in a browser, so it works whether or not intermarche.com offers an API for this.

### What information do I need to provide?

Required: product, store. Optional: review_hash.

### What does it return?

It returns count, lines, total, removed.

### Do I need to be logged in to intermarche.com?

No. It only uses pages of intermarche.com that are reachable without signing in.

### Does it change anything on intermarche.com, or only read data?

It makes changes on intermarche.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/intermarche.com/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/intermarche.com/remove_from_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/intermarche.com/remove_from_cart
