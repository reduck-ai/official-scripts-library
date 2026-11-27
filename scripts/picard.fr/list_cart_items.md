# List Picard cart items

Automatically list Picard cart items on picard.fr. List the items in the Picard France (picard.fr) cart of this browser, as the site holds it: for each line its line id, product id, name, seller (always Picard), quantity, unit price and line price in euros, plus the number of items and the total of the products, delivery and loyalty discounts not included. The offer id is always null: Picard sells only its own products. The cart is the guest cart of the browser, so no sign-in is needed. The prices are the national prices of the French web store when no delivery postcode or store is chosen. An empty cart returns an empty list and a zero count.

- Site: picard.fr
- Address: `reduck/picard.fr/list_cart_items`
- Updated: 2026-11-26 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/picard.fr/list_cart_items`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/picard.fr/list_cart_items
```

## Input

It takes no input.

## Output

- `count` (integer, required): Units in the cart.
- `lines` (array, required)
- `total` (number | null, required): Total of the products in euros, delivery and loyalty discounts not included.
- `currency` (string, required)

## FAQ

### What does "List Picard cart items" do?

List the items in the Picard France (picard.fr) cart of this browser, as the site holds it: for each line its line id, product id, name, seller (always Picard), quantity, unit price and line price in euros, plus the number of items and the total of the products, delivery and loyalty discounts not included. The offer id is always null: Picard sells only its own products. The cart is the guest cart of the browser, so no sign-in is needed. The prices are the national prices of the French web store when no delivery postcode or store is chosen. An empty cart returns an empty list and a zero count.

### How do I automatically list Picard cart items on picard.fr?

Ask an AI agent connected to Reduck to run reduck/picard.fr/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/picard.fr/list_cart_items

### Is there a picard.fr API to list Picard cart items?

You do not need one. "List Picard cart items" drives the real picard.fr pages in a browser, so it works whether or not picard.fr offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns count, lines, total, currency.

### Do I need to be logged in to picard.fr?

No. It only uses pages of picard.fr that are reachable without signing in.

### Does it change anything on picard.fr, or only read data?

It only reads. It looks things up on picard.fr and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/picard.fr/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/picard.fr/list_cart_items

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/picard.fr/list_cart_items
