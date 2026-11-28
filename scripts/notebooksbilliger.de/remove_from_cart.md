# Remove from notebooksbilliger.de cart

Automatically remove from notebooksbilliger.de cart on notebooksbilliger.de. Remove a product's line from the notebooksbilliger.de cart of this browser, by product id, after checking the line is still the one reviewed: pass the review_hash that List notebooksbilliger.de cart items gave for it. If the line changed (quantity or price), nothing is removed and the error gives the line as it is now and its new hash. Returns the cart after the removal; a free add-on that came with the product can stay, at its own price.

- Site: notebooksbilliger.de
- Address: `reduck/notebooksbilliger.de/remove_from_cart`
- Updated: 2026-11-27 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/notebooksbilliger.de/remove_from_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/notebooksbilliger.de/remove_from_cart
```

## Input

- `product` (string, required): The line's productId from List notebooksbilliger.de cart items.
- `review_hash` (string, required): The line's review_hash from List notebooksbilliger.de cart items.

## Output

- `count` (integer, required)
- `lines` (array, required)
- `removed` (object, required)
- `total` (number | null, optional)

## FAQ

### What does "Remove from notebooksbilliger.de cart" do?

Remove a product's line from the notebooksbilliger.de cart of this browser, by product id, after checking the line is still the one reviewed: pass the review_hash that List notebooksbilliger.de cart items gave for it. If the line changed (quantity or price), nothing is removed and the error gives the line as it is now and its new hash. Returns the cart after the removal; a free add-on that came with the product can stay, at its own price.

### How do I automatically remove from notebooksbilliger.de cart on notebooksbilliger.de?

Ask an AI agent connected to Reduck to run reduck/notebooksbilliger.de/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/notebooksbilliger.de/remove_from_cart

### Is there a notebooksbilliger.de API to remove from notebooksbilliger.de cart?

You do not need one. "Remove from notebooksbilliger.de cart" drives the real notebooksbilliger.de pages in a browser, so it works whether or not notebooksbilliger.de offers an API for this.

### What information do I need to provide?

Required: product, review_hash.

### What does it return?

It returns count, lines, total, removed.

### Do I need to be logged in to notebooksbilliger.de?

No. It only uses pages of notebooksbilliger.de that are reachable without signing in.

### Does it change anything on notebooksbilliger.de, or only read data?

It makes changes on notebooksbilliger.de, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/notebooksbilliger.de/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/notebooksbilliger.de/remove_from_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/notebooksbilliger.de/remove_from_cart
