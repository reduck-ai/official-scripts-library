# Get noon product

Automatically get noon product on noon.com. Fetch one noon (noon.com) product by its id (the product_id of Search noon products) or its noon.com product link, in the UAE, Saudi Arabia or Egypt store. Returns title, brand, url, price, list_price, currency, rating, review_count, availability, stock, seller (name, code, rating), express, category_path, image_url, images, feature_bullets, description, specifications and variant options (for example the other colors, each with its product_id and price). Prices are in the currency of the store: UAE dirham, Saudi riyal or Egyptian pound; price is what the offer on the page asks, list_price the struck-through price. Text is in English. An unknown id fails with an error that says so.

- Site: noon.com
- Address: `reduck/noon.com/get-product`
- Updated: 2026-11-24 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/noon.com/get-product`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/noon.com/get-product
```

## Input

- `product` (string, required): The noon product id (for example N53433297A, the product_id of Search noon products) or a noon.com product link.
- `country` (string, optional): The noon store: uae (prices in UAE dirham), saudi (Saudi riyal) or egypt (Egyptian pound).

## Output

- `url` (string, required)
- `title` (string, required)
- `product_id` (string, required)
- `brand` (string | null, optional)
- `price` (number | null, optional)
- `stock` (integer | null, optional): Units the offer has left, as noon reports it.
- `images` (array, optional)
- `rating` (number | null, optional): Average rating out of 5.
- `seller` (object | null, optional)
- `country` (string, optional)
- `express` (boolean | null, optional): True when the offer is fulfilled by noon (noon express).
- `currency` (string, optional)
- `variants` (array, optional): Variant options noon offers, for example each color.
- `image_url` (string | null, optional)
- `brand_code` (string | null, optional)
- `list_price` (number | null, optional): Struck-through price, null when none.
- `description` (string | null, optional)
- `availability` (string, optional)
- `review_count` (integer | null, optional): Number of ratings.
- `category_path` (array, optional)
- `specifications` (array, optional)
- `feature_bullets` (array, optional)

## FAQ

### What does "Get noon product" do?

Fetch one noon (noon.com) product by its id (the product_id of Search noon products) or its noon.com product link, in the UAE, Saudi Arabia or Egypt store. Returns title, brand, url, price, list_price, currency, rating, review_count, availability, stock, seller (name, code, rating), express, category_path, image_url, images, feature_bullets, description, specifications and variant options (for example the other colors, each with its product_id and price). Prices are in the currency of the store: UAE dirham, Saudi riyal or Egyptian pound; price is what the offer on the page asks, list_price the struck-through price. Text is in English. An unknown id fails with an error that says so.

### How do I automatically get noon product on noon.com?

Ask an AI agent connected to Reduck to run reduck/noon.com/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/noon.com/get-product

### Is there a noon.com API to get noon product?

You do not need one. "Get noon product" drives the real noon.com pages in a browser, so it works whether or not noon.com offers an API for this.

### What information do I need to provide?

Required: product. Optional: country.

### What does it return?

It returns url, brand, price, stock, title, images, rating, seller, country, express, currency, variants, image_url, brand_code, list_price, product_id, description, availability, review_count, category_path, specifications, feature_bullets.

### Do I need to be logged in to noon.com?

No. It only uses pages of noon.com that are reachable without signing in.

### Does it change anything on noon.com, or only read data?

It only reads. It looks things up on noon.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/noon.com/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/noon.com/get-product

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/noon.com/get-product
