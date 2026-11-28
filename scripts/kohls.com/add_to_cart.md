# Add to Kohl's cart

Automatically add to Kohl's cart on kohls.com. Add a Kohls.com product to the cart of this browser, by its link and SKU (the page's preselected SKU when none is given), in the given quantity. Refuses a SKU the product does not have or a quantity above what Kohl's can sell. Returns the cart after the add, with a review_hash per line.

- Site: kohls.com
- Address: `reduck/kohls.com/add_to_cart`
- Updated: 2026-11-27 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/kohls.com/add_to_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/kohls.com/add_to_cart
```

## Input

- `url` (string, required): The product's link as Search Kohl's products returns it.
- `sku` (string, optional): The SKU to add, from Get Kohl's product (skus[].sku). Default: the SKU the product page preselects.
- `quantity` (integer, optional)

## Output

- `added` (object, required)
- `count` (integer, required)
- `lines` (array, required)
- `total` (number | null, optional)
- `cartId` (string | null, optional)

## FAQ

### What does "Add to Kohl's cart" do?

Add a Kohls.com product to the cart of this browser, by its link and SKU (the page's preselected SKU when none is given), in the given quantity. Refuses a SKU the product does not have or a quantity above what Kohl's can sell. Returns the cart after the add, with a review_hash per line.

### How do I automatically add to Kohl's cart on kohls.com?

Ask an AI agent connected to Reduck to run reduck/kohls.com/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/kohls.com/add_to_cart

### Is there a kohls.com API to add to Kohl's cart?

You do not need one. "Add to Kohl's cart" drives the real kohls.com pages in a browser, so it works whether or not kohls.com offers an API for this.

### What information do I need to provide?

Required: url. Optional: sku, quantity.

### What does it return?

It returns added, count, lines, total, cartId.

### Do I need to be logged in to kohls.com?

No. It only uses pages of kohls.com that are reachable without signing in.

### Does it change anything on kohls.com, or only read data?

It makes changes on kohls.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/kohls.com/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/kohls.com/add_to_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/kohls.com/add_to_cart
