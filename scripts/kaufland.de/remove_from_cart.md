# Remove from Kaufland cart

Automatically remove from Kaufland cart on kaufland.de. Remove one line from this browser's kaufland.de cart. Takes the line id and its review_hash from List Kaufland cart items, refuses when the line changed since, then returns the cart.

- Site: kaufland.de
- Address: `reduck/kaufland.de/remove_from_cart`
- Updated: 2026-11-27 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/kaufland.de/remove_from_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/kaufland.de/remove_from_cart
```

## Input

- `line_id` (string, required): The line's lineId, as List Kaufland cart items returns it.
- `review_hash` (string, required): The line's review_hash from List Kaufland cart items: proves the line is still what the user reviewed.

## Output

- `count` (integer, required)
- `lines` (array, required)
- `removed` (object, required)
- `total` (number | null, optional)
- `shipping` (number | null, optional)

## FAQ

### What does "Remove from Kaufland cart" do?

Remove one line from this browser's kaufland.de cart. Takes the line id and its review_hash from List Kaufland cart items, refuses when the line changed since, then returns the cart.

### How do I automatically remove from Kaufland cart on kaufland.de?

Ask an AI agent connected to Reduck to run reduck/kaufland.de/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/kaufland.de/remove_from_cart

### Is there a kaufland.de API to remove from Kaufland cart?

You do not need one. "Remove from Kaufland cart" drives the real kaufland.de pages in a browser, so it works whether or not kaufland.de offers an API for this.

### What information do I need to provide?

Required: line_id, review_hash.

### What does it return?

It returns count, lines, total, removed, shipping.

### Do I need to be logged in to kaufland.de?

No. It only uses pages of kaufland.de that are reachable without signing in.

### Does it change anything on kaufland.de, or only read data?

It makes changes on kaufland.de, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/kaufland.de/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/kaufland.de/remove_from_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/kaufland.de/remove_from_cart
