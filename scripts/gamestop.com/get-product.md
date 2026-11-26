# Get GameStop product

Automatically get GameStop product on gamestop.com. Read a GameStop product by id or link: price, availability, condition, platform, rating, images and the variant ids of its other conditions.

- Site: gamestop.com
- Address: `reduck/gamestop.com/get-product`
- Updated: 2026-11-25 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/gamestop.com/get-product`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/gamestop.com/get-product
```

## Input

- `product` (string, required): GameStop product id (variant id such as 425555, or product id such as 20021896) or product link.

## Output

- `id` (string, required): Variant id read (one condition). A product id input reads the variant the site shows first.
- `url` (string | null, required)
- `name` (string | null, required)
- `brand` (string | null, required)
- `price` (number | null, required)
- `images` (array, required)
- `rating` (number | null, required)
- `seller` (string | null, required)
- `edition` (string | null, required)
- `currency` (string | null, required)
- `platform` (string | null, required)
- `preorder` (boolean | null, required)
- `variants` (array, required)
- `available` (boolean | null, required)
- `condition` (string | null, required)
- `publisher` (string | null, required)
- `list_price` (number | null, required)
- `product_id` (string | null, required)
- `availability` (string | null, required)
- `max_quantity` (integer | null, required)
- `review_count` (integer | null, required)

## FAQ

### What does "Get GameStop product" do?

Read a GameStop product by id or link: price, availability, condition, platform, rating, images and the variant ids of its other conditions.

### How do I automatically get GameStop product on gamestop.com?

Ask an AI agent connected to Reduck to run reduck/gamestop.com/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/gamestop.com/get-product

### Is there a gamestop.com API to get GameStop product?

You do not need one. "Get GameStop product" drives the real gamestop.com pages in a browser, so it works whether or not gamestop.com offers an API for this.

### What information do I need to provide?

Required: product.

### What does it return?

It returns id, url, name, brand, price, images, rating, seller, edition, currency, platform, preorder, variants, available, condition, publisher, list_price, product_id, availability, max_quantity, review_count.

### Do I need to be logged in to gamestop.com?

No. It only uses pages of gamestop.com that are reachable without signing in.

### Does it change anything on gamestop.com, or only read data?

It only reads. It looks things up on gamestop.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/gamestop.com/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/gamestop.com/get-product

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/gamestop.com/get-product
