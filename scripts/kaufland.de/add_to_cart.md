# Add to Kaufland cart

Automatically add to Kaufland cart on kaufland.de. Add one seller's offer for a kaufland.de product to this browser's cart, in a quantity from 1 to 10, then return the cart. Takes the product link and, when several sellers offer it, the offer_id that Get Kaufland product offers returns. Nothing is ordered.

- Site: kaufland.de
- Address: `reduck/kaufland.de/add_to_cart`
- Updated: 2026-11-27 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/kaufland.de/add_to_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/kaufland.de/add_to_cart
```

## Input

- `url` (string, required): The product's link as Search Kaufland products returns it (https://www.kaufland.de/product/<id>/).
- `offer_id` (string, optional): The seller's offer to add, as Get Kaufland product offers returns it. Needed when the product has more than one offer.
- `quantity` (integer, optional)

## Output

- `added` (object, required)
- `count` (integer, required)
- `lines` (array, required)
- `total` (number | null, optional)
- `shipping` (number | null, optional)

## FAQ

### What does "Add to Kaufland cart" do?

Add one seller's offer for a kaufland.de product to this browser's cart, in a quantity from 1 to 10, then return the cart. Takes the product link and, when several sellers offer it, the offer_id that Get Kaufland product offers returns. Nothing is ordered.

### How do I automatically add to Kaufland cart on kaufland.de?

Ask an AI agent connected to Reduck to run reduck/kaufland.de/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/kaufland.de/add_to_cart

### Is there a kaufland.de API to add to Kaufland cart?

You do not need one. "Add to Kaufland cart" drives the real kaufland.de pages in a browser, so it works whether or not kaufland.de offers an API for this.

### What information do I need to provide?

Required: url. Optional: offer_id, quantity.

### What does it return?

It returns added, count, lines, total, shipping.

### Do I need to be logged in to kaufland.de?

No. It only uses pages of kaufland.de that are reachable without signing in.

### Does it change anything on kaufland.de, or only read data?

It makes changes on kaufland.de, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/kaufland.de/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/kaufland.de/add_to_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/kaufland.de/add_to_cart
