# Add a product to the Sam's Club cart

Automatically add a product to the Sam's Club cart on samsclub.com. Add a Sam's Club (samsclub.com, US) product to the cart of this browser, by its item id or product link, with a quantity, and return the whole cart afterwards: each line with its line id, product id (the item id), offer id, name, seller, quantity, unit price and line price in US dollars, plus the item count and the subtotal. A product that comes in options (size, color) is added by the item id of one combination, from the variants of Get a Sam's Club product. Works as a guest, with no account: lines already in the cart stay, and units of a product already in the cart are added to its line. Nothing is paid or ordered. An unknown item id, a link that is not a product page, a product Sam's Club does not sell online now, and a quantity above the limit of one order fail with an error that says so.

- Site: samsclub.com
- Address: `reduck/samsclub.com/add_to_cart`
- Updated: 2026-11-26 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/samsclub.com/add_to_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/samsclub.com/add_to_cart
```

## Input

- `url` (string, optional): Sam's Club product link (https://www.samsclub.com/ip/<name>/<item id>). Used when no item_id is given.
- `item_id` (string, optional): Sam's Club item id (productId of Search Sam's Club products, or of one variant of Get a Sam's Club product).
- `quantity` (integer, optional): Number of units to add. Sam's Club limits the quantity of one order per product (maxQuantity of Get a Sam's Club product).

## Output

- `name` (string | null, required)
- `added` (integer, required): Units added by this call.
- `count` (integer, required): Number of items in the cart after the add, all lines together.
- `lines` (array, required)
- `total` (number | null, required): Subtotal of the cart in US dollars, before shipping and tax.
- `offerId` (string | null, required)
- `productId` (string, required): Item id of the product added.

## FAQ

### What does "Add a product to the Sam's Club cart" do?

Add a Sam's Club (samsclub.com, US) product to the cart of this browser, by its item id or product link, with a quantity, and return the whole cart afterwards: each line with its line id, product id (the item id), offer id, name, seller, quantity, unit price and line price in US dollars, plus the item count and the subtotal. A product that comes in options (size, color) is added by the item id of one combination, from the variants of Get a Sam's Club product. Works as a guest, with no account: lines already in the cart stay, and units of a product already in the cart are added to its line. Nothing is paid or ordered. An unknown item id, a link that is not a product page, a product Sam's Club does not sell online now, and a quantity above the limit of one order fail with an error that says so.

### How do I automatically add a product to the Sam's Club cart on samsclub.com?

Ask an AI agent connected to Reduck to run reduck/samsclub.com/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/samsclub.com/add_to_cart

### Is there a samsclub.com API to add a product to the Sam's Club cart?

You do not need one. "Add a product to the Sam's Club cart" drives the real samsclub.com pages in a browser, so it works whether or not samsclub.com offers an API for this.

### What information do I need to provide?

Optional: url, item_id, quantity.

### What does it return?

It returns name, added, count, lines, total, offerId, productId.

### Do I need to be logged in to samsclub.com?

No. It only uses pages of samsclub.com that are reachable without signing in.

### Does it change anything on samsclub.com, or only read data?

It makes changes on samsclub.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/samsclub.com/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/samsclub.com/add_to_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/samsclub.com/add_to_cart
