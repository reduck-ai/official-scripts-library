# List Amazon.es cart items

Automatically list Amazon.es cart items on amazon.es. List the items in your Amazon.es shopping cart: ASIN, title, quantity and unit price, whether each is selected for checkout and whether it is out of stock, plus the cart subtotal. An empty cart returns an empty list. Saved-for-later items are not included. A signed-out browser fails with a signed-out error asking to sign in to amazon.es.

- Site: amazon.es
- Address: `reduck/amazon.es/list_cart_items`
- Updated: 2026-11-25 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/amazon.es/list_cart_items`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/amazon.es/list_cart_items
```

## Input

It takes no input.

## Output

- `items` (array, required)
- `subtotal` (string | null, optional): Subtotal of the selected items, as displayed.

## FAQ

### What does "List Amazon.es cart items" do?

List the items in your Amazon.es shopping cart: ASIN, title, quantity and unit price, whether each is selected for checkout and whether it is out of stock, plus the cart subtotal. An empty cart returns an empty list. Saved-for-later items are not included. A signed-out browser fails with a signed-out error asking to sign in to amazon.es.

### How do I automatically list Amazon.es cart items on amazon.es?

Ask an AI agent connected to Reduck to run reduck/amazon.es/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/amazon.es/list_cart_items

### Is there a amazon.es API to list Amazon.es cart items?

You do not need one. "List Amazon.es cart items" drives the real amazon.es pages in a browser, so it works whether or not amazon.es offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns items, subtotal.

### Do I need to be logged in to amazon.es?

Yes. It acts as you on amazon.es: in your browser it reuses your session, and on a cloud browser it loads your Auth session cookies for amazon.es.

### Does it change anything on amazon.es, or only read data?

It only reads. It looks things up on amazon.es and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/amazon.es/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/amazon.es/list_cart_items

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/amazon.es/list_cart_items
