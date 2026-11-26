# Get Alibaba.com product

Automatically get Alibaba.com product on alibaba.com. Read one Alibaba.com product page by product id or product link: title, price tiers (quantity range and unit price), price range, display currency, minimum order quantity and unit, whether it can go in the cart, the variant attributes and every variant with its variant id, price and stock, the supplier (name, company id, country, years on Alibaba.com, verified mark, response time, on-time delivery rate, rating, business type, store link), the shipping options to the browser's ship-to country (method, fee, delivery time), images, key attributes, category path, rating, review count and sold text. Prices are in the display currency that Alibaba.com sets for the browser. A product that does not exist or is no longer on sale fails with an error that says so. Products that only take a quote request have no shipping options and can_add_to_cart false.

- Site: alibaba.com
- Address: `reduck/alibaba.com/get-product`
- Updated: 2026-11-25 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/alibaba.com/get-product`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/alibaba.com/get-product
```

## Input

- `product_id` (string, required): Alibaba.com product id, as Search Alibaba.com products gives it, or a product page link (www.alibaba.com/product-detail/..._<id>.html).

## Output

- `url` (string, required)
- `title` (string, required)
- `currency` (string | null, required): Three-letter code of the display currency the prices are in, for example EUR.
- `shipping` (object | null, required): Shipping as the page quotes it for the minimum order quantity.
- `supplier` (object, required)
- `variants` (array, required): Every variant, one value of each variant attribute. Empty for a product with no variant.
- `product_id` (string, required)
- `price_tiers` (array, required): Unit price by order quantity, lowest quantity first. Empty when the price depends on the variant only.
- `unit` (string | null, optional): The unit the quantities count, for example piece.
- `images` (array, optional)
- `rating` (number | null, optional)
- `category` (array, optional)
- `price_max` (number | null, optional)
- `price_min` (number | null, optional)
- `sold_text` (string | null, optional)
- `attributes` (array, optional)
- `price_text` (string | null, optional): The price as the page shows it, for example "€6.47-7.40".
- `review_count` (integer | null, optional)
- `can_add_to_cart` (boolean, optional): False for a product that the supplier sells only through a quote request.
- `variant_attributes` (array, optional)
- `minimum_order_quantity` (number | null, optional)

## FAQ

### What does "Get Alibaba.com product" do?

Read one Alibaba.com product page by product id or product link: title, price tiers (quantity range and unit price), price range, display currency, minimum order quantity and unit, whether it can go in the cart, the variant attributes and every variant with its variant id, price and stock, the supplier (name, company id, country, years on Alibaba.com, verified mark, response time, on-time delivery rate, rating, business type, store link), the shipping options to the browser's ship-to country (method, fee, delivery time), images, key attributes, category path, rating, review count and sold text. Prices are in the display currency that Alibaba.com sets for the browser. A product that does not exist or is no longer on sale fails with an error that says so. Products that only take a quote request have no shipping options and can_add_to_cart false.

### How do I automatically get Alibaba.com product on alibaba.com?

Ask an AI agent connected to Reduck to run reduck/alibaba.com/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/alibaba.com/get-product

### Is there a alibaba.com API to get Alibaba.com product?

You do not need one. "Get Alibaba.com product" drives the real alibaba.com pages in a browser, so it works whether or not alibaba.com offers an API for this.

### What information do I need to provide?

Required: product_id.

### What does it return?

It returns url, unit, title, images, rating, category, currency, shipping, supplier, variants, price_max, price_min, sold_text, attributes, price_text, product_id, price_tiers, review_count, can_add_to_cart, variant_attributes, minimum_order_quantity.

### Do I need to be logged in to alibaba.com?

No. It only uses pages of alibaba.com that are reachable without signing in.

### Does it change anything on alibaba.com, or only read data?

It only reads. It looks things up on alibaba.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/alibaba.com/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/alibaba.com/get-product

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/alibaba.com/get-product
