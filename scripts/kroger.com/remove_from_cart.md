# Remove from Kroger cart

Automatically remove from Kroger cart on kroger.com. Remove a product's whole line from the signed-in Kroger.com cart, by UPC, after checking the line is still the one reviewed: pass the review_hash that List Kroger cart items gave for it. If the line changed (quantity or price), nothing is removed and the error gives the line as it is now and its new hash. Returns the cart after the removal.

- Site: kroger.com
- Address: `reduck/kroger.com/remove_from_cart`
- Updated: 2026-11-26 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/kroger.com/remove_from_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/kroger.com/remove_from_cart
```

## Input

- `product` (string, required): The line's productId (13-digit UPC) from List Kroger cart items.
- `review_hash` (string, required): The line's review_hash from List Kroger cart items.

## Output

- `count` (integer, required)
- `lines` (array, required)
- `removed` (object, required)
- `total` (number | null, optional)

## FAQ

### What does "Remove from Kroger cart" do?

Remove a product's whole line from the signed-in Kroger.com cart, by UPC, after checking the line is still the one reviewed: pass the review_hash that List Kroger cart items gave for it. If the line changed (quantity or price), nothing is removed and the error gives the line as it is now and its new hash. Returns the cart after the removal.

### How do I automatically remove from Kroger cart on kroger.com?

Ask an AI agent connected to Reduck to run reduck/kroger.com/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/kroger.com/remove_from_cart

### Is there a kroger.com API to remove from Kroger cart?

You do not need one. "Remove from Kroger cart" drives the real kroger.com pages in a browser, so it works whether or not kroger.com offers an API for this.

### What information do I need to provide?

Required: product, review_hash.

### What does it return?

It returns count, lines, total, removed.

### Do I need to be logged in to kroger.com?

Yes. It acts as you on kroger.com: in your browser it reuses your session, and on a cloud browser it loads your Auth session cookies for kroger.com.

### Does it change anything on kroger.com, or only read data?

It makes changes on kroger.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/kroger.com/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/kroger.com/remove_from_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/kroger.com/remove_from_cart
