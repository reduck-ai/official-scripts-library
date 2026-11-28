# List Intersport cart items

Automatically list Intersport cart items on intersport.fr. List the products in the intersport.fr basket.

- Site: intersport.fr
- Address: `reduck/intersport.fr/list_cart_items`
- Updated: 2026-11-27 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/intersport.fr/list_cart_items`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/intersport.fr/list_cart_items
```

## Input

It takes no input.

## Output

- `items` (array, required)
- `total` (number | null, required): Sum of the lines, before delivery
- `currency` (string, required)
- `item_count` (integer, required)

## FAQ

### What does "List Intersport cart items" do?

List the products in the intersport.fr basket.

### How do I automatically list Intersport cart items on intersport.fr?

Ask an AI agent connected to Reduck to run reduck/intersport.fr/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/intersport.fr/list_cart_items

### Is there a intersport.fr API to list Intersport cart items?

You do not need one. "List Intersport cart items" drives the real intersport.fr pages in a browser, so it works whether or not intersport.fr offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns items, total, currency, item_count.

### Do I need to be logged in to intersport.fr?

No. It only uses pages of intersport.fr that are reachable without signing in.

### Does it change anything on intersport.fr, or only read data?

It only reads. It looks things up on intersport.fr and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/intersport.fr/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/intersport.fr/list_cart_items

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/intersport.fr/list_cart_items
