# List the Dell cart

Automatically list the Dell cart on dell.com. Read the Dell US store cart of this browser: each line with product id, name, quantity, unit price and line price, plus the item subtotal.

- Site: dell.com
- Address: `reduck/dell.com/list_cart_items`
- Updated: 2026-11-25 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/dell.com/list_cart_items`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/dell.com/list_cart_items
```

## Input

It takes no input.

## Output

- `count` (integer, required): Number of units in the cart.
- `lines` (array, required)
- `total` (number | null, required): Item subtotal after discounts, in USD, without tax and shipping.

## FAQ

### What does "List the Dell cart" do?

Read the Dell US store cart of this browser: each line with product id, name, quantity, unit price and line price, plus the item subtotal.

### How do I automatically list the Dell cart on dell.com?

Ask an AI agent connected to Reduck to run reduck/dell.com/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/dell.com/list_cart_items

### Is there a dell.com API to list the Dell cart?

You do not need one. "List the Dell cart" drives the real dell.com pages in a browser, so it works whether or not dell.com offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns count, lines, total.

### Do I need to be logged in to dell.com?

No. It only uses pages of dell.com that are reachable without signing in.

### Does it change anything on dell.com, or only read data?

It only reads. It looks things up on dell.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/dell.com/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/dell.com/list_cart_items

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/dell.com/list_cart_items
