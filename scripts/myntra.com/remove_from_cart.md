# Remove from Myntra bag

Automatically remove from Myntra bag on myntra.com. Remove one line from this browser's myntra.com bag. Takes the line id and its review_hash from List Myntra bag items, refuses when the line changed since, then returns the bag.

- Site: myntra.com
- Address: `reduck/myntra.com/remove_from_cart`
- Updated: 2026-11-27 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/myntra.com/remove_from_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/myntra.com/remove_from_cart
```

## Input

- `line_id` (string, required): The line's lineId, as List Myntra bag items returns it.
- `review_hash` (string, required): The line's review_hash from List Myntra bag items: proves the line is still what the user reviewed.

## Output

- `count` (integer, required)
- `lines` (array, required)
- `removed` (object, required)
- `total` (number | null, optional)

## FAQ

### What does "Remove from Myntra bag" do?

Remove one line from this browser's myntra.com bag. Takes the line id and its review_hash from List Myntra bag items, refuses when the line changed since, then returns the bag.

### How do I automatically remove from Myntra bag on myntra.com?

Ask an AI agent connected to Reduck to run reduck/myntra.com/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/myntra.com/remove_from_cart

### Is there a myntra.com API to remove from Myntra bag?

You do not need one. "Remove from Myntra bag" drives the real myntra.com pages in a browser, so it works whether or not myntra.com offers an API for this.

### What information do I need to provide?

Required: line_id, review_hash.

### What does it return?

It returns count, lines, total, removed.

### Do I need to be logged in to myntra.com?

No. It only uses pages of myntra.com that are reachable without signing in.

### Does it change anything on myntra.com, or only read data?

It makes changes on myntra.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/myntra.com/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/myntra.com/remove_from_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/myntra.com/remove_from_cart
