# Get Cdiscount product

Automatically get Cdiscount product on cdiscount.com. Fetch one Cdiscount.com product page by its sku (the id that Search Cdiscount products returns, for example jbl1200130029967). Returns title, brand, barcode number, manufacturer reference, price and struck-through list_price in euros, rating, review_count, rating_breakdown (number of ratings per star), availability, condition, the seller of the offer shown with its rating, the count and lowest price of the other new and used offers, free_shipping, deals such as Black Friday operations with their end time, breadcrumb, images, description, highlights, the technical attributes and the variants (other colors or sizes, each with its own sku, URL and price). The returned sku can differ from the requested one when Cdiscount opens another variant. An unknown sku fails with an error that says so.

- Site: cdiscount.com
- Address: `reduck/cdiscount.com/get-product`
- Updated: 2026-11-24 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/cdiscount.com/get-product`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/cdiscount.com/get-product
```

## Input

- `sku` (string, required): Cdiscount product id, as Search Cdiscount products returns it (the last part of a product URL, after f-<number>-), for example jbl1200130029967.

## Output

- `sku` (string, required): Sku of the product the page shows.
- `url` (string, required)
- `deals` (array, required): Sales operations on the offer shown, for example Black Week. Empty when there are none.
- `price` (number | null, required): Price in euros of the offer shown.
- `title` (string | null, required)
- `images` (array, required): All product images, large size.
- `rating` (number | null, required): Average stars out of 5, null when there are no reviews.
- `seller` (object | null, required)
- `variants` (array, required): Every variant of the product, this one included. Empty when the product has no variants.
- `attributes` (array, required): Technical specifications, in page order.
- `breadcrumb` (array, required)
- `highlights` (array, required): Key features shown near the title.
- `list_price` (number | null, required): Struck-through reference price in euros, null when none is shown.
- `availability` (string | null, required): schema.org availability the page declares, for example InStock or OutOfStock.
- `review_count` (integer | null, required)
- `requested_sku` (string, required): The sku passed in.
- `ean` (string | null, optional)
- `mpn` (string | null, optional): Manufacturer reference.
- `brand` (string | null, optional)
- `offer_id` (string | null, optional): Id of the seller offer the page shows first.
- `available` (boolean | null, optional): Whether the offer shown can be bought now.
- `condition` (string | null, optional): Condition of a used or refurbished offer as Cdiscount writes it. Null for a new product.
- `image_url` (string | null, optional)
- `description` (string | null, optional)
- `other_offers` (object | null, optional): All offers for this product, the one shown included.
- `free_shipping` (boolean | null, optional)
- `rating_breakdown` (object | null, optional): Number of ratings per star, for example {"5_star": 54, "4_star": 12}. Stars with no rating are left out.

## FAQ

### What does "Get Cdiscount product" do?

Fetch one Cdiscount.com product page by its sku (the id that Search Cdiscount products returns, for example jbl1200130029967). Returns title, brand, barcode number, manufacturer reference, price and struck-through list_price in euros, rating, review_count, rating_breakdown (number of ratings per star), availability, condition, the seller of the offer shown with its rating, the count and lowest price of the other new and used offers, free_shipping, deals such as Black Friday operations with their end time, breadcrumb, images, description, highlights, the technical attributes and the variants (other colors or sizes, each with its own sku, URL and price). The returned sku can differ from the requested one when Cdiscount opens another variant. An unknown sku fails with an error that says so.

### How do I automatically get Cdiscount product on cdiscount.com?

Ask an AI agent connected to Reduck to run reduck/cdiscount.com/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/cdiscount.com/get-product

### Is there a cdiscount.com API to get Cdiscount product?

You do not need one. "Get Cdiscount product" drives the real cdiscount.com pages in a browser, so it works whether or not cdiscount.com offers an API for this.

### What information do I need to provide?

Required: sku.

### What does it return?

It returns ean, mpn, sku, url, brand, deals, price, title, images, rating, seller, offer_id, variants, available, condition, image_url, attributes, breadcrumb, highlights, list_price, description, availability, other_offers, review_count, free_shipping, requested_sku, rating_breakdown.

### Do I need to be logged in to cdiscount.com?

No. It only uses pages of cdiscount.com that are reachable without signing in.

### Does it change anything on cdiscount.com, or only read data?

It only reads. It looks things up on cdiscount.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/cdiscount.com/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/cdiscount.com/get-product

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/cdiscount.com/get-product
