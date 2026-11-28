# List Nocibé cart items

Automatically list Nocibé cart items on nocibe.fr. List the items in the Nocibé (nocibe.fr) cart of this browser, as the site holds it: the number of units, the subtotal of the items in euros (delivery not included), and each line with its item_id (the size code) and review_hash to pass to Remove a product from the Nocibé cart, product id, name, brand, seller (Nocibé or a partner seller), quantity, unit price, list price and line price. The cart is the guest cart of the browser, so no sign-in is needed. An empty cart returns an empty list and a zero count. Works in your own browser (the extension); Nocibé refuses cloud browsers.

- Site: nocibe.fr
- Address: `reduck/nocibe.fr/list_cart_items`
- Updated: 2026-11-27 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/nocibe.fr/list_cart_items`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/nocibe.fr/list_cart_items
```

## Input

It takes no input.

## Output

- `count` (integer, required)
- `items` (array, required)
- `currency` (string, optional)
- `subtotal` (number, optional)

## FAQ

### What does "List Nocibé cart items" do?

List the items in the Nocibé (nocibe.fr) cart of this browser, as the site holds it: the number of units, the subtotal of the items in euros (delivery not included), and each line with its item_id (the size code) and review_hash to pass to Remove a product from the Nocibé cart, product id, name, brand, seller (Nocibé or a partner seller), quantity, unit price, list price and line price. The cart is the guest cart of the browser, so no sign-in is needed. An empty cart returns an empty list and a zero count. Works in your own browser (the extension); Nocibé refuses cloud browsers.

### How do I automatically list Nocibé cart items on nocibe.fr?

Ask an AI agent connected to Reduck to run reduck/nocibe.fr/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/nocibe.fr/list_cart_items

### Is there a nocibe.fr API to list Nocibé cart items?

You do not need one. "List Nocibé cart items" drives the real nocibe.fr pages in a browser, so it works whether or not nocibe.fr offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns count, items, currency, subtotal.

### Do I need to be logged in to nocibe.fr?

No. It only uses pages of nocibe.fr that are reachable without signing in.

### Does it change anything on nocibe.fr, or only read data?

It only reads. It looks things up on nocibe.fr and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/nocibe.fr/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/nocibe.fr/list_cart_items

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/nocibe.fr/list_cart_items
