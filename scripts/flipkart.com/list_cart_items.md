# List the items in the Flipkart cart

Automatically list the items in the Flipkart cart on flipkart.com. List the items in the Flipkart India (flipkart.com) cart of this browser, as the site holds it: for each line its line id, product id, offer id (the seller's listing), name, seller, quantity, unit price and line price in Indian rupees (INR), plus the number of items and the total amount Flipkart shows (it includes the platform fee). The cart is the guest cart of the browser, so no sign-in is needed. Only the main Flipkart cart is read, not the Flipkart Minutes grocery cart. An empty cart returns an empty list, a zero count and a zero total.

- Site: flipkart.com
- Address: `reduck/flipkart.com/list_cart_items`
- Updated: 2026-11-26 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/flipkart.com/list_cart_items`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/flipkart.com/list_cart_items
```

## Input

It takes no input.

## Output

- `count` (integer, required): Number of items in the cart, all lines together.
- `lines` (array, required)
- `total` (number | null, required): Total amount Flipkart shows for the cart, in rupees, with the platform fee.
- `currency` (string, required)

## FAQ

### What does "List the items in the Flipkart cart" do?

List the items in the Flipkart India (flipkart.com) cart of this browser, as the site holds it: for each line its line id, product id, offer id (the seller's listing), name, seller, quantity, unit price and line price in Indian rupees (INR), plus the number of items and the total amount Flipkart shows (it includes the platform fee). The cart is the guest cart of the browser, so no sign-in is needed. Only the main Flipkart cart is read, not the Flipkart Minutes grocery cart. An empty cart returns an empty list, a zero count and a zero total.

### How do I automatically list the items in the Flipkart cart on flipkart.com?

Ask an AI agent connected to Reduck to run reduck/flipkart.com/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/flipkart.com/list_cart_items

### Is there a flipkart.com API to list the items in the Flipkart cart?

You do not need one. "List the items in the Flipkart cart" drives the real flipkart.com pages in a browser, so it works whether or not flipkart.com offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns count, lines, total, currency.

### Do I need to be logged in to flipkart.com?

No. It only uses pages of flipkart.com that are reachable without signing in.

### Does it change anything on flipkart.com, or only read data?

It only reads. It looks things up on flipkart.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/flipkart.com/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/flipkart.com/list_cart_items

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/flipkart.com/list_cart_items
