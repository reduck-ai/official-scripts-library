# List Monoprix cart items

Automatically list Monoprix cart items on monoprix.fr. List the products in the courses.monoprix.fr basket.

- Site: monoprix.fr
- Address: `reduck/monoprix.fr/list_cart_items`
- Updated: 2026-11-27 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/monoprix.fr/list_cart_items`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/monoprix.fr/list_cart_items
```

## Input

It takes no input.

## Output

- `items` (array, required)
- `total` (number | null, required): Basket total after promotions
- `currency` (string, required)
- `item_count` (integer, required): Units in the basket, all lines

## FAQ

### What does "List Monoprix cart items" do?

List the products in the courses.monoprix.fr basket.

### How do I automatically list Monoprix cart items on monoprix.fr?

Ask an AI agent connected to Reduck to run reduck/monoprix.fr/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/monoprix.fr/list_cart_items

### Is there a monoprix.fr API to list Monoprix cart items?

You do not need one. "List Monoprix cart items" drives the real monoprix.fr pages in a browser, so it works whether or not monoprix.fr offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns items, total, currency, item_count.

### Do I need to be logged in to monoprix.fr?

No. It only uses pages of monoprix.fr that are reachable without signing in.

### Does it change anything on monoprix.fr, or only read data?

It only reads. It looks things up on monoprix.fr and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/monoprix.fr/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/monoprix.fr/list_cart_items

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/monoprix.fr/list_cart_items
