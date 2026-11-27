# Get a PetSmart product

Automatically get a PetSmart product on petsmart.com. Read a PetSmart product by SKU or product link: price, availability, rating, images and its size and flavor variants.

- Site: petsmart.com
- Address: `reduck/petsmart.com/get-product`
- Updated: 2026-11-25 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/petsmart.com/get-product`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/petsmart.com/get-product
```

## Input

- `product` (string, required): Product id (SKU or master id, e.g. 5339374) or product link (https://www.petsmart.com/...-5339374.html).

## Output

- `id` (string, required): SKU of the variant the link or id names.
- `url` (string, required)
- `name` (string | null, required)
- `variants` (array, required)
- `size` (string | null, optional)
- `brand` (string | null, optional)
- `price` (number | null, optional)
- `flavor` (string | null, optional)
- `images` (array, optional)
- `rating` (number | null, optional)
- `currency` (string | null, optional)
- `master_id` (string | null, optional)
- `list_price` (number | null, optional)
- `availability` (string | null, optional): schema.org availability, e.g. InStock, OutOfStock.
- `review_count` (integer | null, optional)
- `in_store_only` (boolean | null, optional)

## FAQ

### What does "Get a PetSmart product" do?

Read a PetSmart product by SKU or product link: price, availability, rating, images and its size and flavor variants.

### How do I automatically get a PetSmart product on petsmart.com?

Ask an AI agent connected to Reduck to run reduck/petsmart.com/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/petsmart.com/get-product

### Is there a petsmart.com API to get a PetSmart product?

You do not need one. "Get a PetSmart product" drives the real petsmart.com pages in a browser, so it works whether or not petsmart.com offers an API for this.

### What information do I need to provide?

Required: product.

### What does it return?

It returns id, url, name, size, brand, price, flavor, images, rating, currency, variants, master_id, list_price, availability, review_count, in_store_only.

### Do I need to be logged in to petsmart.com?

No. It only uses pages of petsmart.com that are reachable without signing in.

### Does it change anything on petsmart.com, or only read data?

It only reads. It looks things up on petsmart.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/petsmart.com/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/petsmart.com/get-product

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/petsmart.com/get-product
