# Remove from Kohl's cart

Automatically remove from Kohl's cart on kohls.com. Remove a line from the Kohls.com cart of this browser, by line id, after checking the line is still the one reviewed: pass the review_hash that List Kohl's cart items gave for it. If the line changed (quantity or price), nothing is removed and the error gives the line as it is now and its new hash. Returns the cart after the removal.

- Site: kohls.com
- Address: `reduck/kohls.com/remove_from_cart`
- Updated: 2026-11-27 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/kohls.com/remove_from_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/kohls.com/remove_from_cart
```

## Input

- `line_id` (string, required): The line's lineId from List Kohl's cart items.
- `review_hash` (string, required): The line's review_hash from List Kohl's cart items.

## Output

- `count` (integer, required)
- `lines` (array, required)
- `removed` (object, required)
- `total` (number | null, optional)
- `cartId` (string | null, optional)

## FAQ

### What does "Remove from Kohl's cart" do?

Remove a line from the Kohls.com cart of this browser, by line id, after checking the line is still the one reviewed: pass the review_hash that List Kohl's cart items gave for it. If the line changed (quantity or price), nothing is removed and the error gives the line as it is now and its new hash. Returns the cart after the removal.

### How do I automatically remove from Kohl's cart on kohls.com?

Ask an AI agent connected to Reduck to run reduck/kohls.com/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/kohls.com/remove_from_cart

### Is there a kohls.com API to remove from Kohl's cart?

You do not need one. "Remove from Kohl's cart" drives the real kohls.com pages in a browser, so it works whether or not kohls.com offers an API for this.

### What information do I need to provide?

Required: line_id, review_hash.

### What does it return?

It returns count, lines, total, cartId, removed.

### Do I need to be logged in to kohls.com?

No. It only uses pages of kohls.com that are reachable without signing in.

### Does it change anything on kohls.com, or only read data?

It makes changes on kohls.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/kohls.com/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/kohls.com/remove_from_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/kohls.com/remove_from_cart
