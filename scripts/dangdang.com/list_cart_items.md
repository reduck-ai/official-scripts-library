# List Dangdang cart items

Automatically list Dangdang cart items on dangdang.com. List the items in the shopping cart of this browser on the Dangdang Chinese store (dangdang.com): the item count, the items total in yuan (delivery not included), the currency, and each line with its line id, product id, offer id (always null: Dangdang has one seller for each product), name, seller, quantity, unit price and line price. Works as a guest, with no account: the cart lives in the browser, so a new browser has an empty cart. An empty cart returns an empty list. Use a managed browser in China (country CN): other places can get a slide verification.

- Site: dangdang.com
- Address: `reduck/dangdang.com/list_cart_items`
- Updated: 2026-11-27 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/dangdang.com/list_cart_items`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/dangdang.com/list_cart_items
```

## Input

It takes no input.

## Output

- `count` (integer, required): Units in the cart.
- `lines` (array, required)
- `total` (number, required): Items total in yuan, delivery not included.
- `currency` (string, required)

## FAQ

### What does "List Dangdang cart items" do?

List the items in the shopping cart of this browser on the Dangdang Chinese store (dangdang.com): the item count, the items total in yuan (delivery not included), the currency, and each line with its line id, product id, offer id (always null: Dangdang has one seller for each product), name, seller, quantity, unit price and line price. Works as a guest, with no account: the cart lives in the browser, so a new browser has an empty cart. An empty cart returns an empty list. Use a managed browser in China (country CN): other places can get a slide verification.

### How do I automatically list Dangdang cart items on dangdang.com?

Ask an AI agent connected to Reduck to run reduck/dangdang.com/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/dangdang.com/list_cart_items

### Is there a dangdang.com API to list Dangdang cart items?

You do not need one. "List Dangdang cart items" drives the real dangdang.com pages in a browser, so it works whether or not dangdang.com offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns count, lines, total, currency.

### Do I need to be logged in to dangdang.com?

No. It only uses pages of dangdang.com that are reachable without signing in.

### Does it change anything on dangdang.com, or only read data?

It only reads. It looks things up on dangdang.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/dangdang.com/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/dangdang.com/list_cart_items

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/dangdang.com/list_cart_items
