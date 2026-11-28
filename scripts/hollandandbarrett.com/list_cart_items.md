# List Holland & Barrett cart items

Automatically list Holland & Barrett cart items on hollandandbarrett.com. List the basket of this browser on Holland & Barrett UK (hollandandbarrett.com, the United Kingdom store): each line with its product id, sku (as line id and offer id), name, seller (Holland & Barrett or a marketplace seller), quantity, unit price and line price in pounds (GBP), plus the item count, the basket total with promotions applied (delivery not included) and the currency. Works as a guest, with no account. A browser that never had a basket gives an empty one.

- Site: hollandandbarrett.com
- Address: `reduck/hollandandbarrett.com/list_cart_items`
- Updated: 2026-11-27 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/hollandandbarrett.com/list_cart_items`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/hollandandbarrett.com/list_cart_items
```

## Input

It takes no input.

## Output

- `count` (integer, required): Units in the basket.
- `lines` (array, required)
- `total` (number | null, required): Total of the basket with promotions applied, delivery not included.
- `currency` (string | null, required)

## FAQ

### What does "List Holland & Barrett cart items" do?

List the basket of this browser on Holland & Barrett UK (hollandandbarrett.com, the United Kingdom store): each line with its product id, sku (as line id and offer id), name, seller (Holland & Barrett or a marketplace seller), quantity, unit price and line price in pounds (GBP), plus the item count, the basket total with promotions applied (delivery not included) and the currency. Works as a guest, with no account. A browser that never had a basket gives an empty one.

### How do I automatically list Holland & Barrett cart items on hollandandbarrett.com?

Ask an AI agent connected to Reduck to run reduck/hollandandbarrett.com/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/hollandandbarrett.com/list_cart_items

### Is there a hollandandbarrett.com API to list Holland & Barrett cart items?

You do not need one. "List Holland & Barrett cart items" drives the real hollandandbarrett.com pages in a browser, so it works whether or not hollandandbarrett.com offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns count, lines, total, currency.

### Do I need to be logged in to hollandandbarrett.com?

No. It only uses pages of hollandandbarrett.com that are reachable without signing in.

### Does it change anything on hollandandbarrett.com, or only read data?

It only reads. It looks things up on hollandandbarrett.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/hollandandbarrett.com/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/hollandandbarrett.com/list_cart_items

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/hollandandbarrett.com/list_cart_items
