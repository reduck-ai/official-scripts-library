# List the Harbor Freight cart

Automatically list the Harbor Freight cart on harborfreight.com. List the products in this browser's Harbor Freight guest cart, with quantities, prices and the item subtotal.

- Site: harborfreight.com
- Address: `reduck/harborfreight.com/list_cart_items`
- Updated: 2026-11-25 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/harborfreight.com/list_cart_items`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/harborfreight.com/list_cart_items
```

## Input

It takes no input.

## Output

- `count` (integer, required): Number of units in the cart.
- `lines` (array, required)
- `total` (number | null, optional): Item subtotal, without tax or shipping.

## FAQ

### What does "List the Harbor Freight cart" do?

List the products in this browser's Harbor Freight guest cart, with quantities, prices and the item subtotal.

### How do I automatically list the Harbor Freight cart on harborfreight.com?

Ask an AI agent connected to Reduck to run reduck/harborfreight.com/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/harborfreight.com/list_cart_items

### Is there a harborfreight.com API to list the Harbor Freight cart?

You do not need one. "List the Harbor Freight cart" drives the real harborfreight.com pages in a browser, so it works whether or not harborfreight.com offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns count, lines, total.

### Do I need to be logged in to harborfreight.com?

No. It only uses pages of harborfreight.com that are reachable without signing in.

### Does it change anything on harborfreight.com, or only read data?

It only reads. It looks things up on harborfreight.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/harborfreight.com/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/harborfreight.com/list_cart_items

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/harborfreight.com/list_cart_items
