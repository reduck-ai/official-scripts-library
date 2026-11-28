# Add to La Redoute cart

Automatically add to La Redoute cart on laredoute.fr. Add one variant (colour and size) of a La Redoute product to this browser's basket, in a quantity from 1 to 10, then return the basket. Takes the product link and the variant_id that Get La Redoute product returns. Nothing is ordered.

- Site: laredoute.fr
- Address: `reduck/laredoute.fr/add_to_cart`
- Updated: 2026-11-27 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/laredoute.fr/add_to_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/laredoute.fr/add_to_cart
```

## Input

- `url` (string, required): The product's link as Search La Redoute products returns it (https://www.laredoute.fr/ppdp/prod-<id>.aspx).
- `quantity` (integer, optional)
- `variant_id` (string, optional): The variant (colour and size) to add, as Get La Redoute product returns it (e.g. "1000-1000"). Needed when the product has more than one variant.

## Output

- `added` (object, required)
- `count` (integer, required)
- `lines` (array, required)
- `total` (number | null, optional)

## FAQ

### What does "Add to La Redoute cart" do?

Add one variant (colour and size) of a La Redoute product to this browser's basket, in a quantity from 1 to 10, then return the basket. Takes the product link and the variant_id that Get La Redoute product returns. Nothing is ordered.

### How do I automatically add to La Redoute cart on laredoute.fr?

Ask an AI agent connected to Reduck to run reduck/laredoute.fr/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/laredoute.fr/add_to_cart

### Is there a laredoute.fr API to add to La Redoute cart?

You do not need one. "Add to La Redoute cart" drives the real laredoute.fr pages in a browser, so it works whether or not laredoute.fr offers an API for this.

### What information do I need to provide?

Required: url. Optional: quantity, variant_id.

### What does it return?

It returns added, count, lines, total.

### Do I need to be logged in to laredoute.fr?

No. It only uses pages of laredoute.fr that are reachable without signing in.

### Does it change anything on laredoute.fr, or only read data?

It makes changes on laredoute.fr, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/laredoute.fr/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/laredoute.fr/add_to_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/laredoute.fr/add_to_cart
