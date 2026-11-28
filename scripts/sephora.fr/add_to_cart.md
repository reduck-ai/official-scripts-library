# Add to Sephora France cart

Automatically add to Sephora France cart on sephora.fr. Add one shade or size of a sephora.fr product to this browser's basket, in a quantity from 1 to 10, then return the basket. Takes the product link and, when it has several shades or sizes, the sku that Get Sephora France product returns. Nothing is ordered.

- Site: sephora.fr
- Address: `reduck/sephora.fr/add_to_cart`
- Updated: 2026-11-27 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/sephora.fr/add_to_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/sephora.fr/add_to_cart
```

## Input

- `url` (string, required): The product's link as Search Sephora France products returns it (https://www.sephora.fr/p/....html).
- `sku` (string, optional): The shade or size to add, as Get Sephora France product returns it. Needed when the product has more than one.
- `quantity` (integer, optional)

## Output

- `added` (object, required)
- `count` (integer, required)
- `lines` (array, required)
- `total` (number | null, optional)

## FAQ

### What does "Add to Sephora France cart" do?

Add one shade or size of a sephora.fr product to this browser's basket, in a quantity from 1 to 10, then return the basket. Takes the product link and, when it has several shades or sizes, the sku that Get Sephora France product returns. Nothing is ordered.

### How do I automatically add to Sephora France cart on sephora.fr?

Ask an AI agent connected to Reduck to run reduck/sephora.fr/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/sephora.fr/add_to_cart

### Is there a sephora.fr API to add to Sephora France cart?

You do not need one. "Add to Sephora France cart" drives the real sephora.fr pages in a browser, so it works whether or not sephora.fr offers an API for this.

### What information do I need to provide?

Required: url. Optional: sku, quantity.

### What does it return?

It returns added, count, lines, total.

### Do I need to be logged in to sephora.fr?

No. It only uses pages of sephora.fr that are reachable without signing in.

### Does it change anything on sephora.fr, or only read data?

It makes changes on sephora.fr, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/sephora.fr/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/sephora.fr/add_to_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/sephora.fr/add_to_cart
