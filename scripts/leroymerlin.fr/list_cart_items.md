# List Leroy Merlin cart items

Automatically list Leroy Merlin cart items on leroymerlin.fr. List the items in the Leroy Merlin cart of this browser, as the site holds it: for each line its product reference, offer id, name, seller, quantity, unit price and line price in euros, plus the number of items and the items total (delivery fees excluded). The cart is the guest cart of the browser, so no sign-in is needed. An empty cart returns an empty list, a zero count and a zero total.

- Site: leroymerlin.fr
- Address: `reduck/leroymerlin.fr/list_cart_items`
- Updated: 2026-11-24 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/leroymerlin.fr/list_cart_items`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/leroymerlin.fr/list_cart_items
```

## Input

It takes no input.

## Output

- `count` (integer, required): Units in the cart.
- `lines` (array, required)
- `total` (number | null, required): Items total in euros, taxes included, delivery excluded.

## FAQ

### What does "List Leroy Merlin cart items" do?

List the items in the Leroy Merlin cart of this browser, as the site holds it: for each line its product reference, offer id, name, seller, quantity, unit price and line price in euros, plus the number of items and the items total (delivery fees excluded). The cart is the guest cart of the browser, so no sign-in is needed. An empty cart returns an empty list, a zero count and a zero total.

### How do I automatically list Leroy Merlin cart items on leroymerlin.fr?

Ask an AI agent connected to Reduck to run reduck/leroymerlin.fr/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/leroymerlin.fr/list_cart_items

### Is there a leroymerlin.fr API to list Leroy Merlin cart items?

You do not need one. "List Leroy Merlin cart items" drives the real leroymerlin.fr pages in a browser, so it works whether or not leroymerlin.fr offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns count, lines, total.

### Do I need to be logged in to leroymerlin.fr?

No. It only uses pages of leroymerlin.fr that are reachable without signing in.

### Does it change anything on leroymerlin.fr, or only read data?

It only reads. It looks things up on leroymerlin.fr and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/leroymerlin.fr/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/leroymerlin.fr/list_cart_items

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/leroymerlin.fr/list_cart_items
