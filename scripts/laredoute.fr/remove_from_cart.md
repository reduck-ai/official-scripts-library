# Remove from La Redoute cart

Automatically remove from La Redoute cart on laredoute.fr. Remove one line from this browser's La Redoute basket. Takes the line id and its review_hash from List La Redoute cart items, refuses when the line changed since, then returns the basket.

- Site: laredoute.fr
- Address: `reduck/laredoute.fr/remove_from_cart`
- Updated: 2026-11-27 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/laredoute.fr/remove_from_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/laredoute.fr/remove_from_cart
```

## Input

- `line_id` (string, required): The line's lineId, as List La Redoute cart items returns it.
- `review_hash` (string, required): The line's review_hash from List La Redoute cart items: proves the line is still what the user reviewed.

## Output

- `count` (integer, required)
- `lines` (array, required)
- `removed` (object, required)
- `total` (number | null, optional)

## FAQ

### What does "Remove from La Redoute cart" do?

Remove one line from this browser's La Redoute basket. Takes the line id and its review_hash from List La Redoute cart items, refuses when the line changed since, then returns the basket.

### How do I automatically remove from La Redoute cart on laredoute.fr?

Ask an AI agent connected to Reduck to run reduck/laredoute.fr/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/laredoute.fr/remove_from_cart

### Is there a laredoute.fr API to remove from La Redoute cart?

You do not need one. "Remove from La Redoute cart" drives the real laredoute.fr pages in a browser, so it works whether or not laredoute.fr offers an API for this.

### What information do I need to provide?

Required: line_id, review_hash.

### What does it return?

It returns count, lines, total, removed.

### Do I need to be logged in to laredoute.fr?

No. It only uses pages of laredoute.fr that are reachable without signing in.

### Does it change anything on laredoute.fr, or only read data?

It makes changes on laredoute.fr, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/laredoute.fr/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/laredoute.fr/remove_from_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/laredoute.fr/remove_from_cart
