# List JD Sports cart items

Automatically list JD Sports cart items on jdsports.co.uk. List the shopping bag of this browser on JD Sports UK (jdsports.co.uk, the United Kingdom store): each line with its line id, product id, size sku (offerId), name, size, quantity, unit price and line price in pounds (GBP), plus the item count, the total with promotions applied, the subtotal before them, and the currency. The site can put units of one product on several lines of one unit when a promotion prices them differently. Works as a guest, with no account. A browser that never had a bag gives an empty one.

- Site: jdsports.co.uk
- Address: `reduck/jdsports.co.uk/list_cart_items`
- Updated: 2026-11-27 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/jdsports.co.uk/list_cart_items`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/jdsports.co.uk/list_cart_items
```

## Input

It takes no input.

## Output

- `count` (integer, required): Units in the bag.
- `lines` (array, required)
- `total` (number | null, required): Total of the bag with promotions applied, delivery not chosen.
- `currency` (string | null, required)
- `subtotal` (number | null, required): Total of the bag before promotions.

## FAQ

### What does "List JD Sports cart items" do?

List the shopping bag of this browser on JD Sports UK (jdsports.co.uk, the United Kingdom store): each line with its line id, product id, size sku (offerId), name, size, quantity, unit price and line price in pounds (GBP), plus the item count, the total with promotions applied, the subtotal before them, and the currency. The site can put units of one product on several lines of one unit when a promotion prices them differently. Works as a guest, with no account. A browser that never had a bag gives an empty one.

### How do I automatically list JD Sports cart items on jdsports.co.uk?

Ask an AI agent connected to Reduck to run reduck/jdsports.co.uk/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/jdsports.co.uk/list_cart_items

### Is there a jdsports.co.uk API to list JD Sports cart items?

You do not need one. "List JD Sports cart items" drives the real jdsports.co.uk pages in a browser, so it works whether or not jdsports.co.uk offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns count, lines, total, currency, subtotal.

### Do I need to be logged in to jdsports.co.uk?

No. It only uses pages of jdsports.co.uk that are reachable without signing in.

### Does it change anything on jdsports.co.uk, or only read data?

It only reads. It looks things up on jdsports.co.uk and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/jdsports.co.uk/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/jdsports.co.uk/list_cart_items

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/jdsports.co.uk/list_cart_items
