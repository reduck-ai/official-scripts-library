# Get IKEA France product

Automatically get IKEA France product on ikea.com. Fetch one product of the IKEA France shop (ikea.com/fr/fr) by article number or product link. Returns its name, type, size, description, price in euros, rating, brand, color, categories, images, whether it can be bought online (or only in store, or is coming soon) and its variants such as other sizes or colors, each with its own article number and link. A link or number that is not an IKEA France product fails with an error that says so.

- Site: ikea.com
- Address: `reduck/ikea.com/get-product`
- Updated: 2026-11-25 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/ikea.com/get-product`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/ikea.com/get-product
```

## Input

- `product` (string, required): The 8-digit article number (for example 90132261 or 901.322.61) or the product page link on ikea.com/fr/fr, both returned by Search IKEA France products.

## Output

- `id` (string, required)
- `images` (array, required)
- `category` (array, required)
- `variations` (array, required)
- `url` (string | null, optional)
- `name` (string | null, optional)
- `brand` (string | null, optional)
- `color` (string | null, optional)
- `price` (number | null, optional): The price in large type on the product page. When price_offer_type is "family", it is the IKEA Family member price and a guest pays previous_price.
- `rating` (number | null, optional)
- `currency` (string | null, optional)
- `type_name` (string | null, optional)
- `coming_soon` (boolean | null, optional)
- `description` (string | null, optional)
- `measurement` (string | null, optional)
- `review_count` (integer | null, optional)
- `article_number` (string | null, optional)
- `previous_price` (number | null, optional): The other price the page prints beside the price, e.g. the non-member price, in euros.
- `online_sellable` (boolean | null, optional)
- `price_offer_type` (string | null, optional): The kind of price shown, as the site names it, e.g. "family" for the IKEA Family member price.
- `sold_in_store_only` (boolean | null, optional)
- `previous_price_label` (string | null, optional): The site's label for previous_price, e.g. "Prix non membre".

## FAQ

### What does "Get IKEA France product" do?

Fetch one product of the IKEA France shop (ikea.com/fr/fr) by article number or product link. Returns its name, type, size, description, price in euros, rating, brand, color, categories, images, whether it can be bought online (or only in store, or is coming soon) and its variants such as other sizes or colors, each with its own article number and link. A link or number that is not an IKEA France product fails with an error that says so.

### How do I automatically get IKEA France product on ikea.com?

Ask an AI agent connected to Reduck to run reduck/ikea.com/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/ikea.com/get-product

### Is there a ikea.com API to get IKEA France product?

You do not need one. "Get IKEA France product" drives the real ikea.com pages in a browser, so it works whether or not ikea.com offers an API for this.

### What information do I need to provide?

Required: product.

### What does it return?

It returns id, url, name, brand, color, price, images, rating, category, currency, type_name, variations, coming_soon, description, measurement, review_count, article_number, previous_price, online_sellable, price_offer_type, sold_in_store_only, previous_price_label.

### Do I need to be logged in to ikea.com?

No. It only uses pages of ikea.com that are reachable without signing in.

### Does it change anything on ikea.com, or only read data?

It only reads. It looks things up on ikea.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/ikea.com/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/ikea.com/get-product

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/ikea.com/get-product
