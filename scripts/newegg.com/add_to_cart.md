# Add Newegg product to cart

Automatically add Newegg product to cart on newegg.com. Add 1 to 10 units of a Newegg (newegg.com) product to your cart, from its item number or link, and return the cart after the add. An unknown or unavailable item, or a link that is not a product page, is refused with a clear message.

- Site: newegg.com
- Address: `reduck/newegg.com/add_to_cart`
- Updated: 2026-11-25 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/newegg.com/add_to_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/newegg.com/add_to_cart
```

## Input

- `item` (string, required): Newegg item number (e.g. N82E16820242902) or product URL; search-products, get-product and get-product-offers return it. A marketplace offer has its own item number: pass the offerId from get-product-offers to add that seller's offer.
- `quantity` (integer, optional): Units to add, 1 to 10.

## Output

- `added` (integer, required): Units this run added.
- `count` (integer, required): Total quantity in the cart after the add.
- `lines` (array, required)
- `productId` (string, required)
- `name` (string | null, optional)
- `total` (number | null, optional)
- `offerId` (string | null, optional)

## FAQ

### What does "Add Newegg product to cart" do?

Add 1 to 10 units of a Newegg (newegg.com) product to your cart, from its item number or link, and return the cart after the add. An unknown or unavailable item, or a link that is not a product page, is refused with a clear message.

### How do I automatically add Newegg product to cart on newegg.com?

Ask an AI agent connected to Reduck to run reduck/newegg.com/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/newegg.com/add_to_cart

### Is there a newegg.com API to add Newegg product to cart?

You do not need one. "Add Newegg product to cart" drives the real newegg.com pages in a browser, so it works whether or not newegg.com offers an API for this.

### What information do I need to provide?

Required: item. Optional: quantity.

### What does it return?

It returns name, added, count, lines, total, offerId, productId.

### Do I need to be logged in to newegg.com?

No. It only uses pages of newegg.com that are reachable without signing in.

### Does it change anything on newegg.com, or only read data?

It makes changes on newegg.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/newegg.com/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/newegg.com/add_to_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/newegg.com/add_to_cart
