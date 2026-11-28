# List Galeries Lafayette cart items

Automatically list Galeries Lafayette cart items on galerieslafayette.com. List the products in the galerieslafayette.com basket.

- Site: galerieslafayette.com
- Address: `reduck/galerieslafayette.com/list_cart_items`
- Updated: 2026-11-27 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/galerieslafayette.com/list_cart_items`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/galerieslafayette.com/list_cart_items
```

## Input

It takes no input.

## Output

- `items` (array, required)
- `total` (number | null, required)
- `currency` (string, required)
- `item_count` (integer, required)

## FAQ

### What does "List Galeries Lafayette cart items" do?

List the products in the galerieslafayette.com basket.

### How do I automatically list Galeries Lafayette cart items on galerieslafayette.com?

Ask an AI agent connected to Reduck to run reduck/galerieslafayette.com/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/galerieslafayette.com/list_cart_items

### Is there a galerieslafayette.com API to list Galeries Lafayette cart items?

You do not need one. "List Galeries Lafayette cart items" drives the real galerieslafayette.com pages in a browser, so it works whether or not galerieslafayette.com offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns items, total, currency, item_count.

### Do I need to be logged in to galerieslafayette.com?

No. It only uses pages of galerieslafayette.com that are reachable without signing in.

### Does it change anything on galerieslafayette.com, or only read data?

It only reads. It looks things up on galerieslafayette.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/galerieslafayette.com/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/galerieslafayette.com/list_cart_items

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/galerieslafayette.com/list_cart_items
