# List Amazon.in cart items

Automatically list Amazon.in cart items on amazon.in. List the items in your Amazon.in shopping cart: ASIN, title, quantity and unit price, whether each is selected for checkout and whether it is out of stock, plus the cart subtotal. An empty cart returns an empty list. Saved-for-later items are not included. A signed-out browser fails with a signed-out error asking to sign in to amazon.in.

- Site: amazon.in
- Address: `reduck/amazon.in/list_cart_items`
- Updated: 2026-11-27 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/amazon.in/list_cart_items`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/amazon.in/list_cart_items
```

## Input

It takes no input.

## Output

- `items` (array, required)
- `subtotal` (string | null, optional): Subtotal of the selected items, as displayed.

## FAQ

### What does "List Amazon.in cart items" do?

List the items in your Amazon.in shopping cart: ASIN, title, quantity and unit price, whether each is selected for checkout and whether it is out of stock, plus the cart subtotal. An empty cart returns an empty list. Saved-for-later items are not included. A signed-out browser fails with a signed-out error asking to sign in to amazon.in.

### How do I automatically list Amazon.in cart items on amazon.in?

Ask an AI agent connected to Reduck to run reduck/amazon.in/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/amazon.in/list_cart_items

### Is there a amazon.in API to list Amazon.in cart items?

You do not need one. "List Amazon.in cart items" drives the real amazon.in pages in a browser, so it works whether or not amazon.in offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns items, subtotal.

### Do I need to be logged in to amazon.in?

Yes. It acts as you on amazon.in: in your browser it reuses your session, and on a cloud browser it loads your Auth session cookies for amazon.in.

### Does it change anything on amazon.in, or only read data?

It only reads. It looks things up on amazon.in and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/amazon.in/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/amazon.in/list_cart_items

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/amazon.in/list_cart_items
