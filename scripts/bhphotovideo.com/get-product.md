# Get B&H product

Automatically get B&H product on bhphotovideo.com. Read one B&H Photo Video product page from its B&H item id or link: name, price, availability, rating, brand, images and the options (capacity, color, kit) with their item ids.

- Site: bhphotovideo.com
- Address: `reduck/bhphotovideo.com/get-product`
- Updated: 2026-11-25 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/bhphotovideo.com/get-product`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/bhphotovideo.com/get-product
```

## Input

- `product` (string, required): B&H item id (for example 1948568, with or without its suffix) or a product page link.

## Output

- `id` (string, required): B&H item id, for example 1948568-REG.
- `url` (string, required)
- `images` (array, required)
- `seller` (string, required)
- `variants` (array, required)
- `gtin` (string | null, optional)
- `name` (string | null, optional)
- `brand` (string | null, optional)
- `price` (number | null, optional)
- `rating` (number | null, optional)
- `currency` (string | null, optional)
- `available` (boolean | null, optional)
- `bh_number` (string | null, optional)
- `condition` (string | null, optional)
- `list_price` (number | null, optional): Price before discount, when the page shows one.
- `mfr_number` (string | null, optional)
- `availability` (string | null, optional): schema.org availability, for example InStock.
- `review_count` (integer | null, optional)
- `stock_status` (string | null, optional)

## FAQ

### What does "Get B&H product" do?

Read one B&H Photo Video product page from its B&H item id or link: name, price, availability, rating, brand, images and the options (capacity, color, kit) with their item ids.

### How do I automatically get B&H product on bhphotovideo.com?

Ask an AI agent connected to Reduck to run reduck/bhphotovideo.com/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/bhphotovideo.com/get-product

### Is there a bhphotovideo.com API to get B&H product?

You do not need one. "Get B&H product" drives the real bhphotovideo.com pages in a browser, so it works whether or not bhphotovideo.com offers an API for this.

### What information do I need to provide?

Required: product.

### What does it return?

It returns id, url, gtin, name, brand, price, images, rating, seller, currency, variants, available, bh_number, condition, list_price, mfr_number, availability, review_count, stock_status.

### Do I need to be logged in to bhphotovideo.com?

No. It only uses pages of bhphotovideo.com that are reachable without signing in.

### Does it change anything on bhphotovideo.com, or only read data?

It only reads. It looks things up on bhphotovideo.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/bhphotovideo.com/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/bhphotovideo.com/get-product

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/bhphotovideo.com/get-product
