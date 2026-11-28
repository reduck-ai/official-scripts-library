# Remove Dangdang product from cart

Automatically remove Dangdang product from cart on dangdang.com. Remove a product from the shopping cart of this browser on the Dangdang Chinese store (dangdang.com), by its product id (as List Dangdang cart items returns it), whatever its quantity, as the cart page's delete link does: every line of it, or only the line of one line id. Returns removed and the cart as it is after the removal, in the shape List Dangdang cart items gives. A product that is not in the cart gives removed false and the cart unchanged, not an error. Works as a guest, with no account. Use a managed browser in China (country CN): other places can get a slide verification.

- Site: dangdang.com
- Address: `reduck/dangdang.com/remove_from_cart`
- Updated: 2026-11-27 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/dangdang.com/remove_from_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/dangdang.com/remove_from_cart
```

## Input

- `product` (string, required): Product id as List Dangdang cart items gives it, or a product page link.
- `lineId` (string, optional): Line id from List Dangdang cart items. Leave it out to remove every line of the product.

## Output

- `count` (integer, required): Units in the cart.
- `lines` (array, required)
- `total` (number, required): Items total in yuan, delivery not included.
- `removed` (boolean, required): True when the site removed at least one line.
- `currency` (string, required)

## FAQ

### What does "Remove Dangdang product from cart" do?

Remove a product from the shopping cart of this browser on the Dangdang Chinese store (dangdang.com), by its product id (as List Dangdang cart items returns it), whatever its quantity, as the cart page's delete link does: every line of it, or only the line of one line id. Returns removed and the cart as it is after the removal, in the shape List Dangdang cart items gives. A product that is not in the cart gives removed false and the cart unchanged, not an error. Works as a guest, with no account. Use a managed browser in China (country CN): other places can get a slide verification.

### How do I automatically remove Dangdang product from cart on dangdang.com?

Ask an AI agent connected to Reduck to run reduck/dangdang.com/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/dangdang.com/remove_from_cart

### Is there a dangdang.com API to remove Dangdang product from cart?

You do not need one. "Remove Dangdang product from cart" drives the real dangdang.com pages in a browser, so it works whether or not dangdang.com offers an API for this.

### What information do I need to provide?

Required: product. Optional: lineId.

### What does it return?

It returns count, lines, total, removed, currency.

### Do I need to be logged in to dangdang.com?

No. It only uses pages of dangdang.com that are reachable without signing in.

### Does it change anything on dangdang.com, or only read data?

It makes changes on dangdang.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/dangdang.com/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/dangdang.com/remove_from_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/dangdang.com/remove_from_cart
