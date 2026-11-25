# Get H&M France product

Automatically get H&M France product on hm.com. Read one product page of the H&M France shop (hm.com/fr_fr, prices in euros) by product id, variant id or link: name, brand, description, price, rating, breadcrumb, the sizes of this color each with the variant id to pass to Add H&M France product to cart and whether it is in stock, and the other colors with their own product ids. A product id that does not exist fails with an error that says so.

- Site: hm.com
- Address: `reduck/hm.com/get-product`
- Updated: 2026-11-24 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/hm.com/get-product`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/hm.com/get-product
```

## Input

- `product` (string, required): Product id (10 digits, for example 0685816001; it includes the color), variant id (13 digits, product id plus size code) or a link to an H&M France product page. Ids come from Search H&M France products.

## Output

- `url` (string, required)
- `name` (string | null, required)
- `sizes` (array, required)
- `currency` (string, required)
- `available` (boolean, required)
- `breadcrumb` (array, required)
- `image_urls` (array, required)
- `product_id` (string, required)
- `other_colors` (array, required)
- `brand` (string | null, optional)
- `color` (string | null, optional)
- `price` (number | null, optional)
- `rating` (number | null, optional)
- `description` (string | null, optional)
- `review_count` (integer | null, optional)

## FAQ

### What does "Get H&M France product" do?

Read one product page of the H&M France shop (hm.com/fr_fr, prices in euros) by product id, variant id or link: name, brand, description, price, rating, breadcrumb, the sizes of this color each with the variant id to pass to Add H&M France product to cart and whether it is in stock, and the other colors with their own product ids. A product id that does not exist fails with an error that says so.

### How do I automatically get H&M France product on hm.com?

Ask an AI agent connected to Reduck to run reduck/hm.com/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/hm.com/get-product

### Is there a hm.com API to get H&M France product?

You do not need one. "Get H&M France product" drives the real hm.com pages in a browser, so it works whether or not hm.com offers an API for this.

### What information do I need to provide?

Required: product.

### What does it return?

It returns url, name, brand, color, price, sizes, rating, currency, available, breadcrumb, image_urls, product_id, description, other_colors, review_count.

### Do I need to be logged in to hm.com?

No. It only uses pages of hm.com that are reachable without signing in.

### Does it change anything on hm.com, or only read data?

It only reads. It looks things up on hm.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/hm.com/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/hm.com/get-product

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/hm.com/get-product
