# List H&M France cart items

Automatically list H&M France cart items on hm.com. List the items in the H&M France cart of this browser (hm.com/fr_fr), as the site holds it: for each line the variant id, product id, name, brand, size, color, quantity, unit price and line price in euros, plus the item count and the items subtotal (delivery not included). The cart is the guest cart of the browser, so no sign-in is needed. An empty cart returns an empty list and a zero count.

- Site: hm.com
- Address: `reduck/hm.com/list_cart_items`
- Updated: 2026-11-24 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/hm.com/list_cart_items`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/hm.com/list_cart_items
```

## Input

It takes no input.

## Output

- `count` (integer, required)
- `lines` (array, required)
- `total` (number | null, required)

## FAQ

### What does "List H&M France cart items" do?

List the items in the H&M France cart of this browser (hm.com/fr_fr), as the site holds it: for each line the variant id, product id, name, brand, size, color, quantity, unit price and line price in euros, plus the item count and the items subtotal (delivery not included). The cart is the guest cart of the browser, so no sign-in is needed. An empty cart returns an empty list and a zero count.

### How do I automatically list H&M France cart items on hm.com?

Ask an AI agent connected to Reduck to run reduck/hm.com/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/hm.com/list_cart_items

### Is there a hm.com API to list H&M France cart items?

You do not need one. "List H&M France cart items" drives the real hm.com pages in a browser, so it works whether or not hm.com offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns count, lines, total.

### Do I need to be logged in to hm.com?

No. It only uses pages of hm.com that are reachable without signing in.

### Does it change anything on hm.com, or only read data?

It only reads. It looks things up on hm.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/hm.com/list_cart_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/hm.com/list_cart_items

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/hm.com/list_cart_items
