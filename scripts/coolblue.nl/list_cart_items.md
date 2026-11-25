# List Coolblue cart items

Automatically list Coolblue cart items on coolblue.nl. List the items in the Coolblue Netherlands (coolblue.nl) shopping cart of this browser, as the site holds it: for each line its line id, product number, name, quantity, unit price and line price in euros, plus the number of items and the cart total. The cart is the guest cart of the browser, so no sign-in is needed. An empty cart returns an empty list and a zero count. Offer id and seller are not given by the site and are null.

- Site: coolblue.nl
- Address: `reduck/coolblue.nl/list_cart_items`
- Updated: 2026-11-24 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/coolblue.nl/list_cart_items`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/coolblue.nl/list_cart_items
```

## Input

It takes no input.

## Output

- `count` (integer, required): Number of items in the cart (quantities added up).
- `lines` (array, required)
- `total` (number | null, required): Cart total in euros, VAT included, added up from the lines.

## FAQ

### What does "List Coolblue cart items" do?

List the items in the Coolblue Netherlands (coolblue.nl) shopping cart of this browser, as the site holds it: for each line its line id, product number, name, quantity, unit price and line price in euros, plus the number of items and the cart total. The cart is the guest cart of the browser, so no sign-in is needed. An empty cart returns an empty list and a zero count. Offer id and seller are not given by the site and are null.

### How do I automatically list Coolblue cart items on coolblue.nl?

Ask an AI agent connected to Reduck to run reduck/coolblue.nl/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/coolblue.nl/list_cart_items

### Is there a coolblue.nl API to list Coolblue cart items?

You do not need one. "List Coolblue cart items" drives the real coolblue.nl pages in a browser, so it works whether or not coolblue.nl offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns count, lines, total.

### Do I need to be logged in to coolblue.nl?

No. It only uses pages of coolblue.nl that are reachable without signing in.

### Does it change anything on coolblue.nl, or only read data?

It only reads. It looks things up on coolblue.nl and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/coolblue.nl/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/coolblue.nl/list_cart_items

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/coolblue.nl/list_cart_items
