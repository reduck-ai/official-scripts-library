# List Rue du Commerce cart items

Automatically list Rue du Commerce cart items on rueducommerce.fr. Lists the guest cart of rueducommerce.fr in the browser: each line with product, seller, quantity, unit price and line price in euros, the number of articles and the total. An empty cart returns zero articles and no lines.

- Site: rueducommerce.fr
- Address: `reduck/rueducommerce.fr/list_cart_items`
- Updated: 2026-11-24 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/rueducommerce.fr/list_cart_items`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/rueducommerce.fr/list_cart_items
```

## Input

It takes no input.

## Output

- `count` (integer, required)
- `lines` (array, required)
- `total` (number | null, required)

## FAQ

### What does "List Rue du Commerce cart items" do?

Lists the guest cart of rueducommerce.fr in the browser: each line with product, seller, quantity, unit price and line price in euros, the number of articles and the total. An empty cart returns zero articles and no lines.

### How do I automatically list Rue du Commerce cart items on rueducommerce.fr?

Ask an AI agent connected to Reduck to run reduck/rueducommerce.fr/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/rueducommerce.fr/list_cart_items

### Is there a rueducommerce.fr API to list Rue du Commerce cart items?

You do not need one. "List Rue du Commerce cart items" drives the real rueducommerce.fr pages in a browser, so it works whether or not rueducommerce.fr offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns count, lines, total.

### Do I need to be logged in to rueducommerce.fr?

No. It only uses pages of rueducommerce.fr that are reachable without signing in.

### Does it change anything on rueducommerce.fr, or only read data?

It only reads. It looks things up on rueducommerce.fr and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/rueducommerce.fr/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/rueducommerce.fr/list_cart_items

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/rueducommerce.fr/list_cart_items
