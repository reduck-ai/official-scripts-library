# List Auchan cart items

Automatically list Auchan cart items on auchan.fr. List the items in the Auchan France (auchan.fr) cart of this browser, as the site holds it: for each line its line id, product id, offer id, name with the brand, seller (the drive or Click & Collect store, or the marketplace seller), quantity, unit price and line price in euros, plus the number of items and the cart total. The cart is the guest cart of the browser, so no sign-in is needed; its prices are those of the store this browser chose. An empty cart returns an empty list and a zero count.

- Site: auchan.fr
- Address: `reduck/auchan.fr/list_cart_items`
- Updated: 2026-11-26 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/auchan.fr/list_cart_items`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/auchan.fr/list_cart_items
```

## Input

It takes no input.

## Output

- `count` (integer, required): Units in the cart.
- `lines` (array, required)
- `total` (number | null, required): Cart total in euros.
- `currency` (string, required)

## FAQ

### What does "List Auchan cart items" do?

List the items in the Auchan France (auchan.fr) cart of this browser, as the site holds it: for each line its line id, product id, offer id, name with the brand, seller (the drive or Click & Collect store, or the marketplace seller), quantity, unit price and line price in euros, plus the number of items and the cart total. The cart is the guest cart of the browser, so no sign-in is needed; its prices are those of the store this browser chose. An empty cart returns an empty list and a zero count.

### How do I automatically list Auchan cart items on auchan.fr?

Ask an AI agent connected to Reduck to run reduck/auchan.fr/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/auchan.fr/list_cart_items

### Is there a auchan.fr API to list Auchan cart items?

You do not need one. "List Auchan cart items" drives the real auchan.fr pages in a browser, so it works whether or not auchan.fr offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns count, lines, total, currency.

### Do I need to be logged in to auchan.fr?

No. It only uses pages of auchan.fr that are reachable without signing in.

### Does it change anything on auchan.fr, or only read data?

It only reads. It looks things up on auchan.fr and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/auchan.fr/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/auchan.fr/list_cart_items

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/auchan.fr/list_cart_items
