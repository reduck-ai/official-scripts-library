# List Amazon.com.au cart items

Automatically list Amazon.com.au cart items on amazon.com.au. List the items in your Amazon.com.au shopping cart: ASIN, title, quantity and unit price, whether each is selected for checkout and whether it is out of stock, plus the cart subtotal. An empty cart returns an empty list. Saved-for-later items are not included. A signed-out browser fails with a signed-out error asking to sign in to amazon.com.au.

- Site: amazon.com.au
- Address: `reduck/amazon.com.au/list_cart_items`
- Updated: 2026-11-24 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/amazon.com.au/list_cart_items`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/amazon.com.au/list_cart_items
```

## Input

It takes no input.

## Output

- `items` (array, required)
- `subtotal` (string | null, optional): Subtotal of the selected items, as displayed.

## FAQ

### What does "List Amazon.com.au cart items" do?

List the items in your Amazon.com.au shopping cart: ASIN, title, quantity and unit price, whether each is selected for checkout and whether it is out of stock, plus the cart subtotal. An empty cart returns an empty list. Saved-for-later items are not included. A signed-out browser fails with a signed-out error asking to sign in to amazon.com.au.

### How do I automatically list Amazon.com.au cart items on amazon.com.au?

Ask an AI agent connected to Reduck to run reduck/amazon.com.au/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/amazon.com.au/list_cart_items

### Is there a amazon.com.au API to list Amazon.com.au cart items?

You do not need one. "List Amazon.com.au cart items" drives the real amazon.com.au pages in a browser, so it works whether or not amazon.com.au offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns items, subtotal.

### Do I need to be logged in to amazon.com.au?

Yes. It acts as you on amazon.com.au: in your browser it reuses your session, and on a cloud browser it loads your Auth session cookies for amazon.com.au.

### Does it change anything on amazon.com.au, or only read data?

It only reads. It looks things up on amazon.com.au and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/amazon.com.au/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/amazon.com.au/list_cart_items

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/amazon.com.au/list_cart_items
