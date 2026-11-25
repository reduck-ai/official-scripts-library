# Get Allegro product

Automatically get Allegro product on allegro.pl. Fetch one Allegro (allegro.pl) offer by its offer number (the product_id of Search Allegro products) or by its allegro.pl link. Returns title, price, list_price, currency, rating, rating_count, review_count, availability, condition, available_quantity, brand, gtin, seller (login, id, super seller, positive feedback), catalog_product_id, category_path, image_url and images, parameters and description. Prices are in Polish zloty (PLN); list_price is the struck-through reference price Allegro shows next to a discount. Text is in Polish. An unknown or ended offer fails with an error that says so.

- Site: allegro.pl
- Address: `reduck/allegro.pl/get-product`
- Updated: 2026-11-24 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/allegro.pl/get-product`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/allegro.pl/get-product
```

## Input

- `product` (string, required): The Allegro offer number (for example 18931411486, the product_id of Search Allegro products), or an allegro.pl offer link, or a product link that carries offerId.

## Output

- `url` (string, required)
- `title` (string, required)
- `product_id` (string, required): Allegro offer number.
- `gtin` (string | null, optional)
- `brand` (string | null, optional)
- `price` (number | null, optional): Price in zloty.
- `images` (array, optional)
- `rating` (number | null, optional): Average product rating out of 5.
- `seller` (object | null, optional)
- `currency` (string | null, optional)
- `condition` (string | null, optional): schema.org condition, for example NewCondition or UsedCondition.
- `image_url` (string | null, optional)
- `list_price` (number | null, optional): Struck-through reference price in zloty, null when none.
- `parameters` (array, optional): The offer's parameters (condition, brand, model, and so on), as Allegro lists them.
- `description` (string | null, optional): The seller's description as plain text.
- `availability` (string | null, optional): schema.org availability, for example InStock or OutOfStock.
- `rating_count` (integer | null, optional)
- `review_count` (integer | null, optional): Number of ratings with a written review.
- `category_path` (array, optional): Category path from the top down. The ids are the ones Search Allegro products takes as category_id.
- `available_quantity` (integer | null, optional)
- `catalog_product_id` (string | null, optional): Allegro catalog product of the offer, shared by the offers of the same product.

## FAQ

### What does "Get Allegro product" do?

Fetch one Allegro (allegro.pl) offer by its offer number (the product_id of Search Allegro products) or by its allegro.pl link. Returns title, price, list_price, currency, rating, rating_count, review_count, availability, condition, available_quantity, brand, gtin, seller (login, id, super seller, positive feedback), catalog_product_id, category_path, image_url and images, parameters and description. Prices are in Polish zloty (PLN); list_price is the struck-through reference price Allegro shows next to a discount. Text is in Polish. An unknown or ended offer fails with an error that says so.

### How do I automatically get Allegro product on allegro.pl?

Ask an AI agent connected to Reduck to run reduck/allegro.pl/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/allegro.pl/get-product

### Is there a allegro.pl API to get Allegro product?

You do not need one. "Get Allegro product" drives the real allegro.pl pages in a browser, so it works whether or not allegro.pl offers an API for this.

### What information do I need to provide?

Required: product.

### What does it return?

It returns url, gtin, brand, price, title, images, rating, seller, currency, condition, image_url, list_price, parameters, product_id, description, availability, rating_count, review_count, category_path, available_quantity, catalog_product_id.

### Do I need to be logged in to allegro.pl?

No. It only uses pages of allegro.pl that are reachable without signing in.

### Does it change anything on allegro.pl, or only read data?

It only reads. It looks things up on allegro.pl and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/allegro.pl/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/allegro.pl/get-product

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/allegro.pl/get-product
