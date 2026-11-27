# Add a product to the Flipkart cart

Automatically add a product to the Flipkart cart on flipkart.com. Add a Flipkart India (flipkart.com) product to the cart of this browser, by product id (or product link) and, to choose the seller, an offer id from Get the sellers of a Flipkart product, with a quantity from 1 to 10. Without an offer id, the offer Flipkart picks by default is added. Returns the whole cart afterwards (each line with its line id, product id, offer id, name, seller, quantity, unit price and line price in Indian rupees, the item count and the total amount), plus the product id, offer id and name of what was added and the quantity added. Works as a guest, with no account. Nothing is paid or ordered. An unknown product id, an offer id that is not one of the product's sellers, and a quantity Flipkart refuses fail with an error that says so.

- Site: flipkart.com
- Address: `reduck/flipkart.com/add_to_cart`
- Updated: 2026-11-26 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/flipkart.com/add_to_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/flipkart.com/add_to_cart
```

## Input

- `url` (string, optional): Flipkart product link with pid= in it. Used when no product_id is given.
- `offer_id` (string, optional): Offer id of the seller to buy from, from Get the sellers of a Flipkart product. Omit it for the offer Flipkart picks by default.
- `quantity` (integer, optional): Number of units to add, 1 to 10.
- `product_id` (string, optional): Flipkart product id (16 letters and digits), the product_id of Search Flipkart products.

## Output

- `name` (string | null, required)
- `added` (integer, required): Units added by this call.
- `count` (integer, required): Number of items in the cart after the add, all lines together.
- `lines` (array, required)
- `total` (number | null, required): Total amount Flipkart shows for the cart, in rupees, with the platform fee.
- `offerId` (string, required): Offer id (seller listing) that was added.
- `currency` (string, required)
- `productId` (string, required)

## FAQ

### What does "Add a product to the Flipkart cart" do?

Add a Flipkart India (flipkart.com) product to the cart of this browser, by product id (or product link) and, to choose the seller, an offer id from Get the sellers of a Flipkart product, with a quantity from 1 to 10. Without an offer id, the offer Flipkart picks by default is added. Returns the whole cart afterwards (each line with its line id, product id, offer id, name, seller, quantity, unit price and line price in Indian rupees, the item count and the total amount), plus the product id, offer id and name of what was added and the quantity added. Works as a guest, with no account. Nothing is paid or ordered. An unknown product id, an offer id that is not one of the product's sellers, and a quantity Flipkart refuses fail with an error that says so.

### How do I automatically add a product to the Flipkart cart on flipkart.com?

Ask an AI agent connected to Reduck to run reduck/flipkart.com/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/flipkart.com/add_to_cart

### Is there a flipkart.com API to add a product to the Flipkart cart?

You do not need one. "Add a product to the Flipkart cart" drives the real flipkart.com pages in a browser, so it works whether or not flipkart.com offers an API for this.

### What information do I need to provide?

Optional: url, offer_id, quantity, product_id.

### What does it return?

It returns name, added, count, lines, total, offerId, currency, productId.

### Do I need to be logged in to flipkart.com?

No. It only uses pages of flipkart.com that are reachable without signing in.

### Does it change anything on flipkart.com, or only read data?

It makes changes on flipkart.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/flipkart.com/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/flipkart.com/add_to_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/flipkart.com/add_to_cart
