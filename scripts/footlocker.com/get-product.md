# Get Foot Locker product

Automatically get Foot Locker product on footlocker.com. Get one Foot Locker (footlocker.com, US) product by its id or link: name, brand, color, price and list price in USD, stock, rating, description, its sizes with stock and price, and every color and size variant of the model. An id that Foot Locker does not have gives an error that says so.

- Site: footlocker.com
- Address: `reduck/footlocker.com/get-product`
- Updated: 2026-11-26 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/footlocker.com/get-product`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/footlocker.com/get-product
```

## Input

- `product` (string, required): Product id (the code at the end of a product link, for example CW2288111) or a footlocker.com product link, of one color or of a model.

## Output

- `id` (string, required): Product id (SKU) of the color shown.
- `url` (string, required)
- `name` (string, required)
- `sizes` (array, required)
- `variants` (array, required): Each color and size of the model.
- `brand` (string | null, optional)
- `color` (string | null, optional)
- `price` (number | null, optional): Price now, in USD.
- `rating` (number | null, optional)
- `genders` (array, optional)
- `on_sale` (boolean | null, optional)
- `currency` (string, optional)
- `model_id` (string | null, optional)
- `available` (boolean | null, optional)
- `image_url` (string | null, optional)
- `categories` (array, optional)
- `list_price` (number | null, optional)
- `description` (string | null, optional)
- `launch_date` (string | null, optional)
- `review_count` (number | null, optional)
- `available_to_ship` (boolean | null, optional)

## FAQ

### What does "Get Foot Locker product" do?

Get one Foot Locker (footlocker.com, US) product by its id or link: name, brand, color, price and list price in USD, stock, rating, description, its sizes with stock and price, and every color and size variant of the model. An id that Foot Locker does not have gives an error that says so.

### How do I automatically get Foot Locker product on footlocker.com?

Ask an AI agent connected to Reduck to run reduck/footlocker.com/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/footlocker.com/get-product

### Is there a footlocker.com API to get Foot Locker product?

You do not need one. "Get Foot Locker product" drives the real footlocker.com pages in a browser, so it works whether or not footlocker.com offers an API for this.

### What information do I need to provide?

Required: product.

### What does it return?

It returns id, url, name, brand, color, price, sizes, rating, genders, on_sale, currency, model_id, variants, available, image_url, categories, list_price, description, launch_date, review_count, available_to_ship.

### Do I need to be logged in to footlocker.com?

No. It only uses pages of footlocker.com that are reachable without signing in.

### Does it change anything on footlocker.com, or only read data?

It only reads. It looks things up on footlocker.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/footlocker.com/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/footlocker.com/get-product

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/footlocker.com/get-product
