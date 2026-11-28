# Get Best Buy product

Automatically get Best Buy product on bestbuy.com. Fetch one Best Buy (US) product page by SKU: title, link, main image and all images, brand, model, UPC, category, description, price, regular price, savings, condition, seller (Best Buy or the Marketplace seller's name), rating, review count, specifications, whether it can be added to the cart, the shipping options and delivery dates to a US ZIP code, and the other offers of the same product (other sellers and conditions, each with its own SKU, price and seller), which can be cheaper. A product Best Buy no longer sells comes back with status inactive and no price. An unknown SKU fails with an error that says so.

- Site: bestbuy.com
- Address: `reduck/bestbuy.com/get-product`
- Updated: 2026-11-27 (v4)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/bestbuy.com/get-product`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/bestbuy.com/get-product
```

## Input

- `sku` (string, required): Best Buy SKU (the number after /sku/ in a product link, or the sku of Search Best Buy products), or a bestbuy.com product link that holds one.
- `zipCode` (string, optional): US ZIP code the shipping options and dates are for.

## Output

- `sku` (string, required)
- `url` (string, required): The product page of this SKU.
- `price` (number | null, required): Price in US dollars, before tax and shipping. Null when the product is inactive or Best Buy shows the price only in the cart (price_message).
- `title` (string, required)
- `offers` (array, required): Every offer the page lists for this product, this SKU's included: other sellers and conditions, each its own SKU. Empty for an inactive product.
- `seller` (string | null, required): "Best Buy", or the Marketplace seller's name. Null when the page names none (inactive product).
- `status` (string, required): active, or inactive for a product Best Buy no longer sells.
- `upc` (string | null, optional)
- `brand` (string | null, optional)
- `model` (string | null, optional)
- `images` (array, optional)
- `rating` (number | null, optional)
- `savings` (number | null, optional)
- `category` (string | null, optional)
- `shipping` (object | null, optional): Shipping to zipCode. Null when Best Buy answered nothing for it.
- `condition` (string | null, optional): new, or a used grade such as "refurbished excellent".
- `image_url` (string | null, optional)
- `description` (string | null, optional)
- `button_state` (string | null, optional): Best Buy's state of the add-to-cart button, e.g. ADD_TO_CART, SOLD_OUT, COMING_SOON.
- `review_count` (integer | null, optional)
- `price_message` (string | null, optional)
- `regular_price` (number | null, optional)
- `specifications` (array, optional)
- `can_add_to_cart` (boolean, optional)
- `sold_by_best_buy` (boolean | null, optional)

## FAQ

### What does "Get Best Buy product" do?

Fetch one Best Buy (US) product page by SKU: title, link, main image and all images, brand, model, UPC, category, description, price, regular price, savings, condition, seller (Best Buy or the Marketplace seller's name), rating, review count, specifications, whether it can be added to the cart, the shipping options and delivery dates to a US ZIP code, and the other offers of the same product (other sellers and conditions, each with its own SKU, price and seller), which can be cheaper. A product Best Buy no longer sells comes back with status inactive and no price. An unknown SKU fails with an error that says so.

### How do I automatically get Best Buy product on bestbuy.com?

Ask an AI agent connected to Reduck to run reduck/bestbuy.com/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/bestbuy.com/get-product

### Is there a bestbuy.com API to get Best Buy product?

You do not need one. "Get Best Buy product" drives the real bestbuy.com pages in a browser, so it works whether or not bestbuy.com offers an API for this.

### What information do I need to provide?

Required: sku. Optional: zipCode.

### What does it return?

It returns sku, upc, url, brand, model, price, title, images, offers, rating, seller, status, savings, category, shipping, condition, image_url, description, button_state, review_count, price_message, regular_price, specifications, can_add_to_cart, sold_by_best_buy.

### Do I need to be logged in to bestbuy.com?

No. It only uses pages of bestbuy.com that are reachable without signing in.

### Does it change anything on bestbuy.com, or only read data?

It only reads. It looks things up on bestbuy.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/bestbuy.com/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/bestbuy.com/get-product

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/bestbuy.com/get-product
