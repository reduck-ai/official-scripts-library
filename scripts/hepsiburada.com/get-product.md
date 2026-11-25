# Get Hepsiburada product

Automatically get Hepsiburada product on hepsiburada.com. Fetch one Hepsiburada (hepsiburada.com) product by its id (the product_id of Search Hepsiburada products) or by its hepsiburada.com product link. Returns title, brand, brand_code, url, price, list_price, currency, rating, review_count, availability, seller (name, id, rating out of 10, rating count), category_path, image_url, images, specifications and variants (each with its product_id, name and options, for example its color). Prices are in Turkish lira from the offer the page shows first; list_price is the struck-through price. Text is in Turkish. Offers from other sellers are not included. An unknown id fails with an error that says so.

- Site: hepsiburada.com
- Address: `reduck/hepsiburada.com/get-product`
- Updated: 2026-11-24 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/hepsiburada.com/get-product`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/hepsiburada.com/get-product
```

## Input

- `product` (string, required): The Hepsiburada product id (for example HBCV00004X9ZCH, the product_id of Search Hepsiburada products) or a hepsiburada.com product link.

## Output

- `url` (string, required)
- `title` (string, required)
- `product_id` (string, required): The variant id (HBCV…) of the product the page shows.
- `brand` (string | null, optional)
- `price` (number | null, optional): Price in Turkish lira.
- `images` (array, optional)
- `rating` (number | null, optional): Average rating out of 5.
- `seller` (object | null, optional)
- `currency` (string, optional)
- `variants` (array, optional)
- `image_url` (string | null, optional)
- `brand_code` (string | null, optional): The code Search Hepsiburada products takes in brands.
- `list_price` (number | null, optional): Struck-through price in Turkish lira, null when none.
- `availability` (string, optional)
- `review_count` (integer | null, optional)
- `category_path` (array, optional)
- `specifications` (array, optional)
- `product_group_id` (string | null, optional): The id (HBC…) that groups the variants of the product.

## FAQ

### What does "Get Hepsiburada product" do?

Fetch one Hepsiburada (hepsiburada.com) product by its id (the product_id of Search Hepsiburada products) or by its hepsiburada.com product link. Returns title, brand, brand_code, url, price, list_price, currency, rating, review_count, availability, seller (name, id, rating out of 10, rating count), category_path, image_url, images, specifications and variants (each with its product_id, name and options, for example its color). Prices are in Turkish lira from the offer the page shows first; list_price is the struck-through price. Text is in Turkish. Offers from other sellers are not included. An unknown id fails with an error that says so.

### How do I automatically get Hepsiburada product on hepsiburada.com?

Ask an AI agent connected to Reduck to run reduck/hepsiburada.com/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/hepsiburada.com/get-product

### Is there a hepsiburada.com API to get Hepsiburada product?

You do not need one. "Get Hepsiburada product" drives the real hepsiburada.com pages in a browser, so it works whether or not hepsiburada.com offers an API for this.

### What information do I need to provide?

Required: product.

### What does it return?

It returns url, brand, price, title, images, rating, seller, currency, variants, image_url, brand_code, list_price, product_id, availability, review_count, category_path, specifications, product_group_id.

### Do I need to be logged in to hepsiburada.com?

No. It only uses pages of hepsiburada.com that are reachable without signing in.

### Does it change anything on hepsiburada.com, or only read data?

It only reads. It looks things up on hepsiburada.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/hepsiburada.com/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/hepsiburada.com/get-product

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/hepsiburada.com/get-product
