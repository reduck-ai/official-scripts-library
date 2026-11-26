# Add Lowe's product to cart

Automatically add Lowe's product to cart on lowes.com. Add a Lowes.com product to the cart of this browser, by its link or item id, with a quantity from 1 to 10, and return the whole cart afterwards: each line with its line id, product id (the item id), offer id (always null), name, seller (Lowe's or the marketplace seller), quantity, unit price and line price in US dollars, plus the item count and the subtotal. Works as a guest, with no account: lines already in the cart stay and are listed too. Lowe's picks the fulfillment its page preselects (pickup at the assigned store, or shipping); the same product can then sit on two lines. Nothing is paid or ordered. A product Lowe's does not sell online, an unknown item id and a link that is not a Lowe's product page fail with an error that says so.

- Site: lowes.com
- Address: `reduck/lowes.com/add_to_cart`
- Updated: 2026-11-25 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/lowes.com/add_to_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/lowes.com/add_to_cart
```

## Input

- `url` (string, optional): Lowe's product page link (https://www.lowes.com/pd/<name>/<id>), as returned by Search Lowe's products.
- `item_id` (string, optional): Lowe's item id (item_id of Search Lowe's products). Used when no url is given.
- `quantity` (integer, optional): Number of units to add, 1 to 10.

## Output

- `name` (string | null, required)
- `added` (integer, required): Units added by this call.
- `count` (integer, required): Number of units in the cart after the add, all lines together.
- `lines` (array, required)
- `total` (number | null, required): Subtotal of the cart in US dollars, before tax and delivery.
- `offerId` (string | null, required): Always null: Lowe's has no offer id.
- `productId` (string, required): Lowe's item id of the product added.

## FAQ

### What does "Add Lowe's product to cart" do?

Add a Lowes.com product to the cart of this browser, by its link or item id, with a quantity from 1 to 10, and return the whole cart afterwards: each line with its line id, product id (the item id), offer id (always null), name, seller (Lowe's or the marketplace seller), quantity, unit price and line price in US dollars, plus the item count and the subtotal. Works as a guest, with no account: lines already in the cart stay and are listed too. Lowe's picks the fulfillment its page preselects (pickup at the assigned store, or shipping); the same product can then sit on two lines. Nothing is paid or ordered. A product Lowe's does not sell online, an unknown item id and a link that is not a Lowe's product page fail with an error that says so.

### How do I automatically add Lowe's product to cart on lowes.com?

Ask an AI agent connected to Reduck to run reduck/lowes.com/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/lowes.com/add_to_cart

### Is there a lowes.com API to add Lowe's product to cart?

You do not need one. "Add Lowe's product to cart" drives the real lowes.com pages in a browser, so it works whether or not lowes.com offers an API for this.

### What information do I need to provide?

Optional: url, item_id, quantity.

### What does it return?

It returns name, added, count, lines, total, offerId, productId.

### Do I need to be logged in to lowes.com?

No. It only uses pages of lowes.com that are reachable without signing in.

### Does it change anything on lowes.com, or only read data?

It makes changes on lowes.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/lowes.com/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/lowes.com/add_to_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/lowes.com/add_to_cart
