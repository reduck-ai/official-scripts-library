# List Amazon.fr cart items

Automatically list Amazon.fr cart items on amazon.fr. List the items in your Amazon.fr shopping cart: ASIN, title, quantity and unit price, whether each is selected for checkout and whether it is out of stock, plus the cart subtotal. An empty cart returns an empty list. Saved-for-later items are not included. A signed-out browser fails with a signed-out error asking to sign in to amazon.fr.

- Site: amazon.fr
- Address: `reduck/amazon.fr/list_cart_items`
- Updated: 2026-10-31 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/amazon.fr/list_cart_items`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/amazon.fr/list_cart_items
```

## Input

It takes no input.

## Output

- `items` (array, required)
- `subtotal` (string | null, optional): Subtotal of the selected items, as displayed.

## FAQ

### What does "List Amazon.fr cart items" do?

List the items in your Amazon.fr shopping cart: ASIN, title, quantity and unit price, whether each is selected for checkout and whether it is out of stock, plus the cart subtotal. An empty cart returns an empty list. Saved-for-later items are not included. A signed-out browser fails with a signed-out error asking to sign in to amazon.fr.

### How do I automatically list Amazon.fr cart items on amazon.fr?

Ask an AI agent connected to Reduck to run reduck/amazon.fr/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/amazon.fr/list_cart_items

### Is there a amazon.fr API to list Amazon.fr cart items?

You do not need one. "List Amazon.fr cart items" drives the real amazon.fr pages in a browser, so it works whether or not amazon.fr offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns items, subtotal.

### Do I need to be logged in to amazon.fr?

Yes. It acts as you on amazon.fr: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the amazon.fr cookies saved by the Reduck extension.

### Does it change anything on amazon.fr, or only read data?

It only reads. It looks things up on amazon.fr and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/amazon.fr/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/amazon.fr/list_cart_items

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/amazon.fr/list_cart_items
