# List Home Depot cart items

Automatically list Home Depot cart items on homedepot.com. Returns the homedepot.com cart of this browser (guest or signed in): item count, total and every line with its line id, product id, name, quantity, unit and line price. An empty cart returns count 0 and no lines.

- Site: homedepot.com
- Address: `reduck/homedepot.com/list_cart_items`
- Updated: 2026-11-25 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/homedepot.com/list_cart_items`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/homedepot.com/list_cart_items
```

## Input

It takes no input.

## Output

- `count` (number, required)
- `lines` (array, required)
- `total` (number | null, optional)

## FAQ

### What does "List Home Depot cart items" do?

Returns the homedepot.com cart of this browser (guest or signed in): item count, total and every line with its line id, product id, name, quantity, unit and line price. An empty cart returns count 0 and no lines.

### How do I automatically list Home Depot cart items on homedepot.com?

Ask an AI agent connected to Reduck to run reduck/homedepot.com/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/homedepot.com/list_cart_items

### Is there a homedepot.com API to list Home Depot cart items?

You do not need one. "List Home Depot cart items" drives the real homedepot.com pages in a browser, so it works whether or not homedepot.com offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns count, lines, total.

### Do I need to be logged in to homedepot.com?

No. It only uses pages of homedepot.com that are reachable without signing in.

### Does it change anything on homedepot.com, or only read data?

It only reads. It looks things up on homedepot.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/homedepot.com/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/homedepot.com/list_cart_items

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/homedepot.com/list_cart_items
