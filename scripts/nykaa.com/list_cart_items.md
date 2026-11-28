# List Nykaa bag items

Automatically list Nykaa bag items on nykaa.com. List the bag (cart) of this browser in the Nykaa India store (nykaa.com): each line with its line id, product id, name, seller, quantity, unit price and line price, plus the number of units and the grand total, in Indian rupees. It reads the guest bag when nobody is signed in; Nykaa needs no delivery pincode for it. An empty bag returns no lines and a null total.

- Site: nykaa.com
- Address: `reduck/nykaa.com/list_cart_items`
- Updated: 2026-11-27 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/nykaa.com/list_cart_items`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/nykaa.com/list_cart_items
```

## Input

It takes no input.

## Output

- `count` (integer, required): Number of units in the bag.
- `lines` (array, required)
- `total` (number | null, required): Grand total of the bag in Indian rupees. Null when the bag is empty.
- `currency` (string, required): INR

## FAQ

### What does "List Nykaa bag items" do?

List the bag (cart) of this browser in the Nykaa India store (nykaa.com): each line with its line id, product id, name, seller, quantity, unit price and line price, plus the number of units and the grand total, in Indian rupees. It reads the guest bag when nobody is signed in; Nykaa needs no delivery pincode for it. An empty bag returns no lines and a null total.

### How do I automatically list Nykaa bag items on nykaa.com?

Ask an AI agent connected to Reduck to run reduck/nykaa.com/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/nykaa.com/list_cart_items

### Is there a nykaa.com API to list Nykaa bag items?

You do not need one. "List Nykaa bag items" drives the real nykaa.com pages in a browser, so it works whether or not nykaa.com offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns count, lines, total, currency.

### Do I need to be logged in to nykaa.com?

No. It only uses pages of nykaa.com that are reachable without signing in.

### Does it change anything on nykaa.com, or only read data?

It only reads. It looks things up on nykaa.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/nykaa.com/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/nykaa.com/list_cart_items

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/nykaa.com/list_cart_items
