# List bol.com cart items

Automatically list bol.com cart items on bol.com. List the items in the bol.com cart (Netherlands, Dutch site) of this browser, as the site holds it: for each line its product id, offer id, name, seller, quantity, unit price and line price in euros, plus the number of items and the total of the articles in euros (delivery not included). The cart is the guest cart of the browser, so no sign-in is needed. An empty cart returns an empty list, a zero count and no total.

- Site: bol.com
- Address: `reduck/bol.com/list_cart_items`
- Updated: 2026-11-24 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/bol.com/list_cart_items`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/bol.com/list_cart_items
```

## Input

It takes no input.

## Output

- `count` (integer, required): Units in the cart.
- `lines` (array, required)
- `total` (number | null, required): Total of the articles in euros, delivery not included.

## FAQ

### What does "List bol.com cart items" do?

List the items in the bol.com cart (Netherlands, Dutch site) of this browser, as the site holds it: for each line its product id, offer id, name, seller, quantity, unit price and line price in euros, plus the number of items and the total of the articles in euros (delivery not included). The cart is the guest cart of the browser, so no sign-in is needed. An empty cart returns an empty list, a zero count and no total.

### How do I automatically list bol.com cart items on bol.com?

Ask an AI agent connected to Reduck to run reduck/bol.com/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/bol.com/list_cart_items

### Is there a bol.com API to list bol.com cart items?

You do not need one. "List bol.com cart items" drives the real bol.com pages in a browser, so it works whether or not bol.com offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns count, lines, total.

### Do I need to be logged in to bol.com?

No. It only uses pages of bol.com that are reachable without signing in.

### Does it change anything on bol.com, or only read data?

It only reads. It looks things up on bol.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/bol.com/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/bol.com/list_cart_items

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/bol.com/list_cart_items
