# List Brico Depot cart items

Automatically list Brico Depot cart items on bricodepot.fr. List the items in the Brico Depot (bricodepot.fr) shopping cart of this browser, as the site holds it: the item count, the items total in euros (taxes included, delivery not included) and each line with its line id, product id (the sku), offer id (always null), name, seller (always Brico Dépôt), quantity, unit price and line price. The cart is the guest cart of the browser, so no sign-in is needed. An empty cart, or a browser that has no cart yet, returns an empty list and a zero count.

- Site: bricodepot.fr
- Address: `reduck/bricodepot.fr/list_cart_items`
- Updated: 2026-11-25 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/bricodepot.fr/list_cart_items`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/bricodepot.fr/list_cart_items
```

## Input

It takes no input.

## Output

- `count` (integer, required): Units in the cart.
- `lines` (array, required)
- `total` (number | null, required): Items total in euros, taxes included, delivery not included.

## FAQ

### What does "List Brico Depot cart items" do?

List the items in the Brico Depot (bricodepot.fr) shopping cart of this browser, as the site holds it: the item count, the items total in euros (taxes included, delivery not included) and each line with its line id, product id (the sku), offer id (always null), name, seller (always Brico Dépôt), quantity, unit price and line price. The cart is the guest cart of the browser, so no sign-in is needed. An empty cart, or a browser that has no cart yet, returns an empty list and a zero count.

### How do I automatically list Brico Depot cart items on bricodepot.fr?

Ask an AI agent connected to Reduck to run reduck/bricodepot.fr/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/bricodepot.fr/list_cart_items

### Is there a bricodepot.fr API to list Brico Depot cart items?

You do not need one. "List Brico Depot cart items" drives the real bricodepot.fr pages in a browser, so it works whether or not bricodepot.fr offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns count, lines, total.

### Do I need to be logged in to bricodepot.fr?

No. It only uses pages of bricodepot.fr that are reachable without signing in.

### Does it change anything on bricodepot.fr, or only read data?

It only reads. It looks things up on bricodepot.fr and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/bricodepot.fr/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/bricodepot.fr/list_cart_items

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/bricodepot.fr/list_cart_items
