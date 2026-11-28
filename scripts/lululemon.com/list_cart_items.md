# List lululemon cart items

Automatically list lululemon cart items on lululemon.com. List the products in the shop.lululemon.com bag.

- Site: lululemon.com
- Address: `reduck/lululemon.com/list_cart_items`
- Updated: 2026-11-27 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/lululemon.com/list_cart_items`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/lululemon.com/list_cart_items
```

## Input

It takes no input.

## Output

- `items` (array, required)
- `item_count` (integer, required)
- `currency` (string, optional)
- `subtotal` (number | null, optional)

## FAQ

### What does "List lululemon cart items" do?

List the products in the shop.lululemon.com bag.

### How do I automatically list lululemon cart items on lululemon.com?

Ask an AI agent connected to Reduck to run reduck/lululemon.com/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/lululemon.com/list_cart_items

### Is there a lululemon.com API to list lululemon cart items?

You do not need one. "List lululemon cart items" drives the real lululemon.com pages in a browser, so it works whether or not lululemon.com offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns items, currency, subtotal, item_count.

### Do I need to be logged in to lululemon.com?

No. It only uses pages of lululemon.com that are reachable without signing in.

### Does it change anything on lululemon.com, or only read data?

It only reads. It looks things up on lululemon.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/lululemon.com/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/lululemon.com/list_cart_items

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/lululemon.com/list_cart_items
