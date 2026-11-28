# List E.Leclerc cart items

Automatically list E.Leclerc cart items on e.leclerc. List the products in the e.leclerc basket.

- Site: e.leclerc
- Address: `reduck/e.leclerc/list_cart_items`
- Updated: 2026-11-27 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/e.leclerc/list_cart_items`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/e.leclerc/list_cart_items
```

## Input

It takes no input.

## Output

- `items` (array, required)
- `total` (number | null, required): Basket total before shipping
- `currency` (string, required)
- `item_count` (integer, required)

## FAQ

### What does "List E.Leclerc cart items" do?

List the products in the e.leclerc basket.

### How do I automatically list E.Leclerc cart items on e.leclerc?

Ask an AI agent connected to Reduck to run reduck/e.leclerc/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/e.leclerc/list_cart_items

### Is there a e.leclerc API to list E.Leclerc cart items?

You do not need one. "List E.Leclerc cart items" drives the real e.leclerc pages in a browser, so it works whether or not e.leclerc offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns items, total, currency, item_count.

### Do I need to be logged in to e.leclerc?

No. It only uses pages of e.leclerc that are reachable without signing in.

### Does it change anything on e.leclerc, or only read data?

It only reads. It looks things up on e.leclerc and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/e.leclerc/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/e.leclerc/list_cart_items

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/e.leclerc/list_cart_items
