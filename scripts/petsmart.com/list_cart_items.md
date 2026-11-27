# List the PetSmart cart items

Automatically list the PetSmart cart items on petsmart.com. List the products in the PetSmart cart with quantities, prices and the item subtotal.

- Site: petsmart.com
- Address: `reduck/petsmart.com/list_cart_items`
- Updated: 2026-11-25 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/petsmart.com/list_cart_items`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/petsmart.com/list_cart_items
```

## Input

It takes no input.

## Output

- `count` (integer, required)
- `lines` (array, required)
- `total` (number | null, optional): Item subtotal in USD, without tax and shipping.

## FAQ

### What does "List the PetSmart cart items" do?

List the products in the PetSmart cart with quantities, prices and the item subtotal.

### How do I automatically list the PetSmart cart items on petsmart.com?

Ask an AI agent connected to Reduck to run reduck/petsmart.com/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/petsmart.com/list_cart_items

### Is there a petsmart.com API to list the PetSmart cart items?

You do not need one. "List the PetSmart cart items" drives the real petsmart.com pages in a browser, so it works whether or not petsmart.com offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns count, lines, total.

### Do I need to be logged in to petsmart.com?

No. It only uses pages of petsmart.com that are reachable without signing in.

### Does it change anything on petsmart.com, or only read data?

It only reads. It looks things up on petsmart.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/petsmart.com/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/petsmart.com/list_cart_items

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/petsmart.com/list_cart_items
