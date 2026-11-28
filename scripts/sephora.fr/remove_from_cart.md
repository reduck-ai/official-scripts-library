# Remove from Sephora France cart

Automatically remove from Sephora France cart on sephora.fr. Remove one line from this browser's sephora.fr basket. Takes the line id and its review_hash from List Sephora France cart items, refuses when the line changed since, then returns the basket.

- Site: sephora.fr
- Address: `reduck/sephora.fr/remove_from_cart`
- Updated: 2026-11-27 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/sephora.fr/remove_from_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/sephora.fr/remove_from_cart
```

## Input

- `line_id` (string, required): The line's lineId, as List Sephora France cart items returns it.
- `review_hash` (string, required): The line's review_hash from List Sephora France cart items: proves the line is still what the user reviewed.

## Output

- `count` (integer, required)
- `lines` (array, required)
- `removed` (object, required)
- `total` (number | null, optional)

## FAQ

### What does "Remove from Sephora France cart" do?

Remove one line from this browser's sephora.fr basket. Takes the line id and its review_hash from List Sephora France cart items, refuses when the line changed since, then returns the basket.

### How do I automatically remove from Sephora France cart on sephora.fr?

Ask an AI agent connected to Reduck to run reduck/sephora.fr/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/sephora.fr/remove_from_cart

### Is there a sephora.fr API to remove from Sephora France cart?

You do not need one. "Remove from Sephora France cart" drives the real sephora.fr pages in a browser, so it works whether or not sephora.fr offers an API for this.

### What information do I need to provide?

Required: line_id, review_hash.

### What does it return?

It returns count, lines, total, removed.

### Do I need to be logged in to sephora.fr?

No. It only uses pages of sephora.fr that are reachable without signing in.

### Does it change anything on sephora.fr, or only read data?

It makes changes on sephora.fr, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/sephora.fr/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/sephora.fr/remove_from_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/sephora.fr/remove_from_cart
