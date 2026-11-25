# Get Decathlon product

Automatically get Decathlon product on decathlon.fr. Fetch one Decathlon.fr product page from its link (as returned by Search Decathlon products). Returns the title, brand, description, rating and review count, the color shown, the images, and the variants of that color: each size with its sku id (the id that Add Decathlon product to cart takes), offer id, price and struck-through list price in euros, the seller (Decathlon or a marketplace seller), the condition and whether it can be bought. Also lists the other colors of the product with their link. A link that is not a Decathlon product page fails with an error that says so.

- Site: decathlon.fr
- Address: `reduck/decathlon.fr/get-product`
- Updated: 2026-11-24 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/decathlon.fr/get-product`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/decathlon.fr/get-product
```

## Input

- `url` (string, required): Link of the product page (https://www.decathlon.fr/p/...), as returned by Search Decathlon products.

## Output

- `url` (string, required)
- `title` (string | null, required)
- `variants` (array, required)
- `brand` (string | null, optional)
- `color` (string | null, optional)
- `images` (array, optional)
- `rating` (number | null, optional)
- `model_id` (string | null, optional)
- `description` (string | null, optional)
- `other_colors` (array, optional)
- `review_count` (integer | null, optional)
- `item_group_id` (string | null, optional)

## FAQ

### What does "Get Decathlon product" do?

Fetch one Decathlon.fr product page from its link (as returned by Search Decathlon products). Returns the title, brand, description, rating and review count, the color shown, the images, and the variants of that color: each size with its sku id (the id that Add Decathlon product to cart takes), offer id, price and struck-through list price in euros, the seller (Decathlon or a marketplace seller), the condition and whether it can be bought. Also lists the other colors of the product with their link. A link that is not a Decathlon product page fails with an error that says so.

### How do I automatically get Decathlon product on decathlon.fr?

Ask an AI agent connected to Reduck to run reduck/decathlon.fr/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/decathlon.fr/get-product

### Is there a decathlon.fr API to get Decathlon product?

You do not need one. "Get Decathlon product" drives the real decathlon.fr pages in a browser, so it works whether or not decathlon.fr offers an API for this.

### What information do I need to provide?

Required: url.

### What does it return?

It returns url, brand, color, title, images, rating, model_id, variants, description, other_colors, review_count, item_group_id.

### Do I need to be logged in to decathlon.fr?

No. It only uses pages of decathlon.fr that are reachable without signing in.

### Does it change anything on decathlon.fr, or only read data?

It only reads. It looks things up on decathlon.fr and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/decathlon.fr/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/decathlon.fr/get-product

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/decathlon.fr/get-product
