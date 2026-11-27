# Get Rakuten product

Automatically get Rakuten product on rakuten.co.jp. Fetch one Rakuten Ichiba (rakuten.co.jp) product by its id (shop-code/item-code, as Search Rakuten products returns it) or by its item.rakuten.co.jp link. Returns title, tagline, price and price_max, list_price, currency, rating, review_count, availability, condition, shop, genre_id, breadcrumb, image_url and images, description, attributes, and variants (each with its options, price, stock and availability). Prices are in Japanese yen (JPY), tax included; price is the lowest variant price. Text is in Japanese, as the shop writes it. An unknown id fails with an error that says so.

- Site: rakuten.co.jp
- Address: `reduck/rakuten.co.jp/get-product`
- Updated: 2026-11-24 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/rakuten.co.jp/get-product`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/rakuten.co.jp/get-product
```

## Input

- `product` (string, required): The product id as shop-code/item-code (for example kamaya-awards/ip15mtm-100, the product_id of Search Rakuten products), or an item.rakuten.co.jp product link.

## Output

- `url` (string, required)
- `title` (string, required)
- `product_id` (string, required): shop-code/item-code.
- `shop` (object, optional)
- `price` (number | null, optional): Lowest variant price in yen, tax included.
- `images` (array, optional)
- `rating` (number | null, optional): Average review score out of 5, null when there is no review.
- `tagline` (string | null, optional): The short catch line under the title, when the shop sets one.
- `currency` (string, optional): Always JPY.
- `genre_id` (string | null, optional): Rakuten genre id, which Search Rakuten products takes as genre_id.
- `variants` (array, optional): One entry per variant the shop sells. Empty for an item without variants.
- `condition` (string | null, optional): Item condition as Rakuten records it, for example new or used.
- `image_url` (string | null, optional)
- `price_max` (number | null, optional): Highest variant price in yen when the variants have different prices, else null.
- `attributes` (array, optional): Product attributes the shop declares (brand, model, and so on), from the first variant.
- `breadcrumb` (array, optional)
- `list_price` (number | null, optional): Reference price in yen the shop shows struck through, null when none.
- `description` (string | null, optional): Product description as plain text.
- `availability` (string | null, optional): Null when the shop publishes no stock information.
- `review_count` (integer | null, optional)

## FAQ

### What does "Get Rakuten product" do?

Fetch one Rakuten Ichiba (rakuten.co.jp) product by its id (shop-code/item-code, as Search Rakuten products returns it) or by its item.rakuten.co.jp link. Returns title, tagline, price and price_max, list_price, currency, rating, review_count, availability, condition, shop, genre_id, breadcrumb, image_url and images, description, attributes, and variants (each with its options, price, stock and availability). Prices are in Japanese yen (JPY), tax included; price is the lowest variant price. Text is in Japanese, as the shop writes it. An unknown id fails with an error that says so.

### How do I automatically get Rakuten product on rakuten.co.jp?

Ask an AI agent connected to Reduck to run reduck/rakuten.co.jp/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/rakuten.co.jp/get-product

### Is there a rakuten.co.jp API to get Rakuten product?

You do not need one. "Get Rakuten product" drives the real rakuten.co.jp pages in a browser, so it works whether or not rakuten.co.jp offers an API for this.

### What information do I need to provide?

Required: product.

### What does it return?

It returns url, shop, price, title, images, rating, tagline, currency, genre_id, variants, condition, image_url, price_max, attributes, breadcrumb, list_price, product_id, description, availability, review_count.

### Do I need to be logged in to rakuten.co.jp?

No. It only uses pages of rakuten.co.jp that are reachable without signing in.

### Does it change anything on rakuten.co.jp, or only read data?

It only reads. It looks things up on rakuten.co.jp and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/rakuten.co.jp/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/rakuten.co.jp/get-product

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/rakuten.co.jp/get-product
