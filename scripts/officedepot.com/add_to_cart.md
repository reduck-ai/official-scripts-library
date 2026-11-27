# Add Office Depot product to cart

Automatically add Office Depot product to cart on officedepot.com. Add an OfficeDepot.com product to the cart of this browser, by its link or item number, with a quantity from 1 to 99, and return the whole cart afterwards: each line with its line id, product id (the item number), offer id, name, seller (Office Depot or the marketplace seller), quantity, unit price and line price in US dollars, plus the item count and the subtotal. Works as a guest, with no account: lines already in the cart stay and are listed too. Office Depot adds the item for delivery to the ZIP code it assigns to a new guest browser. Nothing is paid or ordered. A product that cannot be added to the cart, an unknown item number and a link that is not an Office Depot product page fail with an error that says so.

- Site: officedepot.com
- Address: `reduck/officedepot.com/add_to_cart`
- Updated: 2026-11-26 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/officedepot.com/add_to_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/officedepot.com/add_to_cart
```

## Input

- `url` (string, optional): Office Depot product page link (https://www.officedepot.com/a/products/<number>/<name>/), as returned by Search Office Depot products.
- `quantity` (integer, optional): Number of units to add, 1 to 99.
- `product_id` (string, optional): Office Depot item number (product_id of Search Office Depot products). Used when no url is given.

## Output

- `name` (string | null, required)
- `added` (integer, required): Units added by this call.
- `count` (integer, required): Number of units in the cart after the add, all lines together.
- `lines` (array, required)
- `total` (number | null, required): Subtotal of the cart in US dollars, before tax and delivery.
- `offerId` (string | null, required): Marketplace offer id of the product added; null when Office Depot sells it.
- `productId` (string, required): Office Depot item number of the product added.

## FAQ

### What does "Add Office Depot product to cart" do?

Add an OfficeDepot.com product to the cart of this browser, by its link or item number, with a quantity from 1 to 99, and return the whole cart afterwards: each line with its line id, product id (the item number), offer id, name, seller (Office Depot or the marketplace seller), quantity, unit price and line price in US dollars, plus the item count and the subtotal. Works as a guest, with no account: lines already in the cart stay and are listed too. Office Depot adds the item for delivery to the ZIP code it assigns to a new guest browser. Nothing is paid or ordered. A product that cannot be added to the cart, an unknown item number and a link that is not an Office Depot product page fail with an error that says so.

### How do I automatically add Office Depot product to cart on officedepot.com?

Ask an AI agent connected to Reduck to run reduck/officedepot.com/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/officedepot.com/add_to_cart

### Is there a officedepot.com API to add Office Depot product to cart?

You do not need one. "Add Office Depot product to cart" drives the real officedepot.com pages in a browser, so it works whether or not officedepot.com offers an API for this.

### What information do I need to provide?

Optional: url, quantity, product_id.

### What does it return?

It returns name, added, count, lines, total, offerId, productId.

### Do I need to be logged in to officedepot.com?

No. It only uses pages of officedepot.com that are reachable without signing in.

### Does it change anything on officedepot.com, or only read data?

It makes changes on officedepot.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/officedepot.com/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/officedepot.com/add_to_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/officedepot.com/add_to_cart
