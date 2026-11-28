# Add to Myntra bag

Automatically add to Myntra bag on myntra.com. Add one size of a myntra.com product to this browser's bag, in a quantity from 1 to 5, then return the bag. Takes the product link, the sku of the size from Get Myntra product, and optionally a seller_id from Get Myntra product offers. Nothing is ordered.

- Site: myntra.com
- Address: `reduck/myntra.com/add_to_cart`
- Updated: 2026-11-27 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/myntra.com/add_to_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/myntra.com/add_to_cart
```

## Input

- `url` (string, required): The product's link as Search Myntra products returns it (https://www.myntra.com/.../<id>/buy).
- `sku` (string, optional): The size to add, as Get Myntra product returns it. Needed when the product has more than one size.
- `quantity` (integer, optional)
- `seller_id` (string, optional): The seller to buy from, as Get Myntra product offers returns it. Default: the seller Myntra shows for that size.

## Output

- `added` (object, required)
- `count` (integer, required)
- `lines` (array, required)
- `total` (number | null, optional)

## FAQ

### What does "Add to Myntra bag" do?

Add one size of a myntra.com product to this browser's bag, in a quantity from 1 to 5, then return the bag. Takes the product link, the sku of the size from Get Myntra product, and optionally a seller_id from Get Myntra product offers. Nothing is ordered.

### How do I automatically add to Myntra bag on myntra.com?

Ask an AI agent connected to Reduck to run reduck/myntra.com/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/myntra.com/add_to_cart

### Is there a myntra.com API to add to Myntra bag?

You do not need one. "Add to Myntra bag" drives the real myntra.com pages in a browser, so it works whether or not myntra.com offers an API for this.

### What information do I need to provide?

Required: url. Optional: sku, quantity, seller_id.

### What does it return?

It returns added, count, lines, total.

### Do I need to be logged in to myntra.com?

No. It only uses pages of myntra.com that are reachable without signing in.

### Does it change anything on myntra.com, or only read data?

It makes changes on myntra.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/myntra.com/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/myntra.com/add_to_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/myntra.com/add_to_cart
