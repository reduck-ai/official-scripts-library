# List ManoMano cart items

Automatically list ManoMano cart items on manomano.fr. List the items in the ManoMano.fr cart of this browser, as the site holds it: for each line its product id, name, the seller that ships it, quantity, unit price and line price in euros, plus the number of items and the total of the products, delivery not included. The cart is the guest cart of the browser, so no sign-in is needed. An empty cart returns an empty list and a zero count.

- Site: manomano.fr
- Address: `reduck/manomano.fr/list_cart_items`
- Updated: 2026-11-24 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/manomano.fr/list_cart_items`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/manomano.fr/list_cart_items
```

## Input

It takes no input.

## Output

- `count` (integer, required): Units in the cart.
- `lines` (array, required)
- `total` (number | null, required): Total of the products in euros, taxes included, delivery not included.

## FAQ

### What does "List ManoMano cart items" do?

List the items in the ManoMano.fr cart of this browser, as the site holds it: for each line its product id, name, the seller that ships it, quantity, unit price and line price in euros, plus the number of items and the total of the products, delivery not included. The cart is the guest cart of the browser, so no sign-in is needed. An empty cart returns an empty list and a zero count.

### How do I automatically list ManoMano cart items on manomano.fr?

Ask an AI agent connected to Reduck to run reduck/manomano.fr/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/manomano.fr/list_cart_items

### Is there a manomano.fr API to list ManoMano cart items?

You do not need one. "List ManoMano cart items" drives the real manomano.fr pages in a browser, so it works whether or not manomano.fr offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns count, lines, total.

### Do I need to be logged in to manomano.fr?

No. It only uses pages of manomano.fr that are reachable without signing in.

### Does it change anything on manomano.fr, or only read data?

It only reads. It looks things up on manomano.fr and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/manomano.fr/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/manomano.fr/list_cart_items

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/manomano.fr/list_cart_items
