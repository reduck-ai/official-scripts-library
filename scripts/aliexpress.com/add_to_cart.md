# Add AliExpress product to cart

Automatically add AliExpress product to cart on aliexpress.com. Add an AliExpress product to the cart of this browser from its id or product page link, with an optional sku_id (the variant: color, size) and a quantity from 1 to 10, and return the cart afterwards: each line with its line id, product id, offer id (the sku id), name, seller, quantity, unit price and line price, plus the unit count and the total. Without sku_id, the variant the product page selects is added. Works as a guest, with no account: the cart lives in the browser, so lines already in it stay and are listed too. Nothing is paid or ordered. An unknown product, a product AliExpress does not sell in the browser's region, an unknown or sold-out sku and a link that is not a product page fail with an error.

- Site: aliexpress.com
- Address: `reduck/aliexpress.com/add_to_cart`
- Updated: 2026-11-26 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/aliexpress.com/add_to_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/aliexpress.com/add_to_cart
```

## Input

- `product` (string, required): AliExpress product id (the id of Search AliExpress products) or the link of a product page (https://www.aliexpress.com/item/<id>.html, any country site).
- `sku_id` (string, optional): Sku id of the variant to add (color, size...), from the variants of Get AliExpress product. Leave out to add the variant the product page selects.
- `quantity` (integer, optional): Number of units to add, 1 to 10.

## Output

- `name` (string | null, required)
- `added` (integer, required): Number of units added.
- `count` (integer, required): Number of units in the cart after the add.
- `lines` (array, required)
- `total` (number | null, required): Sum of the line prices, shipping not included.
- `offerId` (string | null, required): The sku id that was added.
- `productId` (string, required)
- `currency` (string | null, optional)

## FAQ

### What does "Add AliExpress product to cart" do?

Add an AliExpress product to the cart of this browser from its id or product page link, with an optional sku_id (the variant: color, size) and a quantity from 1 to 10, and return the cart afterwards: each line with its line id, product id, offer id (the sku id), name, seller, quantity, unit price and line price, plus the unit count and the total. Without sku_id, the variant the product page selects is added. Works as a guest, with no account: the cart lives in the browser, so lines already in it stay and are listed too. Nothing is paid or ordered. An unknown product, a product AliExpress does not sell in the browser's region, an unknown or sold-out sku and a link that is not a product page fail with an error.

### How do I automatically add AliExpress product to cart on aliexpress.com?

Ask an AI agent connected to Reduck to run reduck/aliexpress.com/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/aliexpress.com/add_to_cart

### Is there a aliexpress.com API to add AliExpress product to cart?

You do not need one. "Add AliExpress product to cart" drives the real aliexpress.com pages in a browser, so it works whether or not aliexpress.com offers an API for this.

### What information do I need to provide?

Required: product. Optional: sku_id, quantity.

### What does it return?

It returns name, added, count, lines, total, offerId, currency, productId.

### Do I need to be logged in to aliexpress.com?

No. It only uses pages of aliexpress.com that are reachable without signing in.

### Does it change anything on aliexpress.com, or only read data?

It makes changes on aliexpress.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/aliexpress.com/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/aliexpress.com/add_to_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/aliexpress.com/add_to_cart
