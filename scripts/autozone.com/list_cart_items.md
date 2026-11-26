# List the AutoZone cart items

Automatically list the AutoZone cart items on autozone.com. List the products in the AutoZone cart with quantity, unit price and line price, plus the item count and the item subtotal.

- Site: autozone.com
- Address: `reduck/autozone.com/list_cart_items`
- Updated: 2026-11-25 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/autozone.com/list_cart_items`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/autozone.com/list_cart_items
```

## Input

It takes no input.

## Output

- `count` (integer, required): Number of items in the cart (sum of quantities).
- `lines` (array, required)
- `total` (number | null, required): Item subtotal in USD, without tax or shipping.

## FAQ

### What does "List the AutoZone cart items" do?

List the products in the AutoZone cart with quantity, unit price and line price, plus the item count and the item subtotal.

### How do I automatically list the AutoZone cart items on autozone.com?

Ask an AI agent connected to Reduck to run reduck/autozone.com/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/autozone.com/list_cart_items

### Is there a autozone.com API to list the AutoZone cart items?

You do not need one. "List the AutoZone cart items" drives the real autozone.com pages in a browser, so it works whether or not autozone.com offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns count, lines, total.

### Do I need to be logged in to autozone.com?

No. It only uses pages of autozone.com that are reachable without signing in.

### Does it change anything on autozone.com, or only read data?

It only reads. It looks things up on autozone.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/autozone.com/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/autozone.com/list_cart_items

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/autozone.com/list_cart_items
