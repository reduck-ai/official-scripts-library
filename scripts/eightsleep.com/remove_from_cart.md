# Remove a line from the Eight Sleep cart

Automatically remove a line from the Eight Sleep cart on eightsleep.com. Remove one line, with all its quantity, from the Eight Sleep US guest cart of this browser, and return the cart after the change. Get line ids from eightsleep.com/list_cart_items. When the cart has no such line, the cart does not change and removed is false.

- Site: eightsleep.com
- Address: `reduck/eightsleep.com/remove_from_cart`
- Updated: 2026-11-27 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/eightsleep.com/remove_from_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/eightsleep.com/remove_from_cart
```

## Input

- `lineId` (string, required): The line id from eightsleep.com/list_cart_items, e.g. cali_01M8EKC52R3ST5S2WY1EFHTVQ3.

## Output

- `count` (integer, required)
- `lines` (array, required)
- `total` (number, required): Cart total before tax, in US dollars.
- `removed` (boolean, required)

## FAQ

### What does "Remove a line from the Eight Sleep cart" do?

Remove one line, with all its quantity, from the Eight Sleep US guest cart of this browser, and return the cart after the change. Get line ids from eightsleep.com/list_cart_items. When the cart has no such line, the cart does not change and removed is false.

### How do I automatically remove a line from the Eight Sleep cart on eightsleep.com?

Ask an AI agent connected to Reduck to run reduck/eightsleep.com/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/eightsleep.com/remove_from_cart

### Is there a eightsleep.com API to remove a line from the Eight Sleep cart?

You do not need one. "Remove a line from the Eight Sleep cart" drives the real eightsleep.com pages in a browser, so it works whether or not eightsleep.com offers an API for this.

### What information do I need to provide?

Required: lineId.

### What does it return?

It returns count, lines, total, removed.

### Do I need to be logged in to eightsleep.com?

No. It only uses pages of eightsleep.com that are reachable without signing in.

### Does it change anything on eightsleep.com, or only read data?

It makes changes on eightsleep.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/eightsleep.com/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/eightsleep.com/remove_from_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/eightsleep.com/remove_from_cart
