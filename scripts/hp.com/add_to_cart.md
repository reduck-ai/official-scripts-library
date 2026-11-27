# Add a product to the HP cart

Automatically add a product to the HP cart on hp.com. Add a fixed HP model (product class STO) of the HP US store (hp.com/us-en/shop) to the cart of this browser, by its link or HP part number, with a quantity from 1 to 10, and return the whole cart afterwards: each line with its line id, product id (the HP part number), offer id (always null), name, seller (always HP), quantity, unit price and line price in US dollars, plus the item count and the products total before tax and shipping. Works as a guest, with no account: lines already in the cart stay and are listed too. Nothing is paid or ordered. A customizable model (CTO), an out of stock product, an unknown part number and a link that is not an HP product page fail with an error that says so.

- Site: hp.com
- Address: `reduck/hp.com/add_to_cart`
- Updated: 2026-11-26 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/hp.com/add_to_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/hp.com/add_to_cart
```

## Input

- `url` (string, optional): HP US store product link (https://www.hp.com/us-en/shop/pdp/...), as Search HP products returns it.
- `quantity` (integer, optional): Number of units to add, 1 to 10.
- `product_id` (string, optional): HP part number, for example 7P8K6AV_1 (product_id of Search HP products). Used when no url is given.

## Output

- `name` (string | null, required)
- `added` (integer, required): Units added by this call.
- `count` (integer, required): Number of units in the cart after the add, all lines together.
- `lines` (array, required)
- `total` (number | null, required): Total of the products in US dollars, before tax and shipping.
- `offerId` (string | null, required): Always null: HP sells its products itself.
- `productId` (string, required): HP part number of the product added.

## FAQ

### What does "Add a product to the HP cart" do?

Add a fixed HP model (product class STO) of the HP US store (hp.com/us-en/shop) to the cart of this browser, by its link or HP part number, with a quantity from 1 to 10, and return the whole cart afterwards: each line with its line id, product id (the HP part number), offer id (always null), name, seller (always HP), quantity, unit price and line price in US dollars, plus the item count and the products total before tax and shipping. Works as a guest, with no account: lines already in the cart stay and are listed too. Nothing is paid or ordered. A customizable model (CTO), an out of stock product, an unknown part number and a link that is not an HP product page fail with an error that says so.

### How do I automatically add a product to the HP cart on hp.com?

Ask an AI agent connected to Reduck to run reduck/hp.com/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/hp.com/add_to_cart

### Is there a hp.com API to add a product to the HP cart?

You do not need one. "Add a product to the HP cart" drives the real hp.com pages in a browser, so it works whether or not hp.com offers an API for this.

### What information do I need to provide?

Optional: url, quantity, product_id.

### What does it return?

It returns name, added, count, lines, total, offerId, productId.

### Do I need to be logged in to hp.com?

No. It only uses pages of hp.com that are reachable without signing in.

### Does it change anything on hp.com, or only read data?

It makes changes on hp.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/hp.com/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/hp.com/add_to_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/hp.com/add_to_cart
