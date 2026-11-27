# Get Flipkart product

Automatically get Flipkart product on flipkart.com. Fetch one Flipkart India (flipkart.com) product by its id (the product_id of Search Flipkart products) or by its flipkart.com product link. Returns title, brand, url, price, list_price, currency, rating, rating_count, review_count, rating_breakdown, availability, seller (id, name, rating), flipkart_assured, category_path, image_url, images and the variant attributes of this product (for example its color). Prices are in Indian rupees (INR) as a visitor with no delivery address sees them; list_price is the struck-through maximum retail price. Bank and exchange offers are not included. An unknown id fails with an error that says so.

- Site: flipkart.com
- Address: `reduck/flipkart.com/get-product`
- Updated: 2026-11-26 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/flipkart.com/get-product`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/flipkart.com/get-product
```

## Input

- `product` (string, required): The Flipkart product id (16 letters and digits, for example MOBGTAGPTB3VS24W, the product_id of Search Flipkart products) or a flipkart.com product link that has pid= in it.

## Output

- `url` (string, required)
- `title` (string, required)
- `product_id` (string, required)
- `brand` (string | null, optional)
- `price` (number | null, optional): Selling price in rupees.
- `images` (array, optional)
- `rating` (number | null, optional): Average rating out of 5.
- `seller` (object | null, optional)
- `currency` (string | null, optional): INR.
- `image_url` (string | null, optional)
- `attributes` (array, optional): Variant attributes of this product, for example its color or size.
- `list_price` (number | null, optional): Struck-through maximum retail price in rupees, null when none.
- `availability` (string | null, optional): Flipkart's stock state, for example IN_STOCK or OUT_OF_STOCK.
- `rating_count` (integer | null, optional)
- `review_count` (integer | null, optional): Number of written reviews.
- `category_path` (array, optional): Category names from the top category down.
- `flipkart_assured` (boolean | null, optional)
- `rating_breakdown` (object | null, optional): Number of ratings per star, for example {"5": 194956}.

## FAQ

### What does "Get Flipkart product" do?

Fetch one Flipkart India (flipkart.com) product by its id (the product_id of Search Flipkart products) or by its flipkart.com product link. Returns title, brand, url, price, list_price, currency, rating, rating_count, review_count, rating_breakdown, availability, seller (id, name, rating), flipkart_assured, category_path, image_url, images and the variant attributes of this product (for example its color). Prices are in Indian rupees (INR) as a visitor with no delivery address sees them; list_price is the struck-through maximum retail price. Bank and exchange offers are not included. An unknown id fails with an error that says so.

### How do I automatically get Flipkart product on flipkart.com?

Ask an AI agent connected to Reduck to run reduck/flipkart.com/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/flipkart.com/get-product

### Is there a flipkart.com API to get Flipkart product?

You do not need one. "Get Flipkart product" drives the real flipkart.com pages in a browser, so it works whether or not flipkart.com offers an API for this.

### What information do I need to provide?

Required: product.

### What does it return?

It returns url, brand, price, title, images, rating, seller, currency, image_url, attributes, list_price, product_id, availability, rating_count, review_count, category_path, flipkart_assured, rating_breakdown.

### Do I need to be logged in to flipkart.com?

No. It only uses pages of flipkart.com that are reachable without signing in.

### Does it change anything on flipkart.com, or only read data?

It only reads. It looks things up on flipkart.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/flipkart.com/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/flipkart.com/get-product

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/flipkart.com/get-product
