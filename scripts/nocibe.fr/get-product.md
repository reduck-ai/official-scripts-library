# Get Nocibé product

Automatically get Nocibé product on nocibe.fr. Get one product of the Nocibé French beauty store (nocibe.fr) from its product id (for example 5012090029, or M002796015 for a partner seller's product), the code of one size, or its product link: name, brand, line, category and categories, description, bullet points, gender, rating and review count, the seller (Nocibé or a partner seller), the maximum quantity per order, images, and every size with its offer_id (the code to pass to Add a product to the Nocibé cart), size label, price, list price, discount, price per 100 ml or per kg, stock and availability text. selected_offer_id is the size the link names (?variant=). An id or link Nocibé does not know is refused with an error. Each size has one seller, so there is no offers script. Works in your own browser (the extension); Nocibé refuses cloud browsers.

- Site: nocibe.fr
- Address: `reduck/nocibe.fr/get-product`
- Updated: 2026-11-27 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/nocibe.fr/get-product`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/nocibe.fr/get-product
```

## Input

- `product` (string, required): The product id (product_id from Search Nocibé products, e.g. 5012090029 or M002796015 for a partner seller's product), the code of one size, or a nocibe.fr product link.

## Output

- `id` (string, required)
- `url` (string, required)
- `line` (string | null, optional)
- `name` (string | null, optional)
- `brand` (string | null, optional)
- `gender` (string | null, optional)
- `rating` (number | null, optional)
- `seller` (string | null, optional)
- `bullets` (array, optional)
- `category` (string | null, optional)
- `variants` (array, optional)
- `categories` (array, optional)
- `image_urls` (array, optional)
- `description` (string | null, optional)
- `marketplace` (boolean, optional)
- `max_quantity` (integer | null, optional)
- `review_count` (integer | null, optional)
- `selected_offer_id` (string | null, optional)

## FAQ

### What does "Get Nocibé product" do?

Get one product of the Nocibé French beauty store (nocibe.fr) from its product id (for example 5012090029, or M002796015 for a partner seller's product), the code of one size, or its product link: name, brand, line, category and categories, description, bullet points, gender, rating and review count, the seller (Nocibé or a partner seller), the maximum quantity per order, images, and every size with its offer_id (the code to pass to Add a product to the Nocibé cart), size label, price, list price, discount, price per 100 ml or per kg, stock and availability text. selected_offer_id is the size the link names (?variant=). An id or link Nocibé does not know is refused with an error. Each size has one seller, so there is no offers script. Works in your own browser (the extension); Nocibé refuses cloud browsers.

### How do I automatically get Nocibé product on nocibe.fr?

Ask an AI agent connected to Reduck to run reduck/nocibe.fr/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/nocibe.fr/get-product

### Is there a nocibe.fr API to get Nocibé product?

You do not need one. "Get Nocibé product" drives the real nocibe.fr pages in a browser, so it works whether or not nocibe.fr offers an API for this.

### What information do I need to provide?

Required: product.

### What does it return?

It returns id, url, line, name, brand, gender, rating, seller, bullets, category, variants, categories, image_urls, description, marketplace, max_quantity, review_count, selected_offer_id.

### Do I need to be logged in to nocibe.fr?

No. It only uses pages of nocibe.fr that are reachable without signing in.

### Does it change anything on nocibe.fr, or only read data?

It only reads. It looks things up on nocibe.fr and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/nocibe.fr/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/nocibe.fr/get-product

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/nocibe.fr/get-product
