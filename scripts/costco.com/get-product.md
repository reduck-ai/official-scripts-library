# Get Costco product

Automatically get Costco product on costco.com. Fetch one Costco.com product page from its product id (the number at the end of a costco.com/p/... link, e.g. 4000410259) or the link itself: name, brand, Costco item number, online price in US dollars, availability, rating and rating count, image, description, feature bullets and breadcrumb, as the page states them. Prices are the signed-out online price (null on members-only items). A link that is not a product page fails with an error. Costco answers an unknown product id and a refused browser the same way (HTTP 429, empty page), so both fail with one error that says so.

- Site: costco.com
- Address: `reduck/costco.com/get-product`
- Updated: 2026-11-25 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/costco.com/get-product`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/costco.com/get-product
```

## Input

- `product` (string, optional): The product id (the digits at the end of a costco.com/p/... link, e.g. 4000410259) or the product page link itself.
- `product_id` (string, optional): Older form of the same input: the product id only. Pass `product` instead.

## Output

- `url` (string, required)
- `name` (string, required)
- `product_id` (string, required)
- `brand` (string | null, optional)
- `price` (number | null, optional): Online price as the page states it.
- `rating` (number | null, optional)
- `currency` (string | null, optional)
- `features` (array, optional)
- `image_url` (string | null, optional)
- `breadcrumb` (array, optional)
- `description` (string | null, optional)
- `item_number` (string | null, optional): Costco item number (the page's Item #).
- `availability` (string | null, optional): schema.org availability as the page states it, e.g. InStock or OutOfStock.
- `rating_count` (integer | null, optional)

## FAQ

### What does "Get Costco product" do?

Fetch one Costco.com product page from its product id (the number at the end of a costco.com/p/... link, e.g. 4000410259) or the link itself: name, brand, Costco item number, online price in US dollars, availability, rating and rating count, image, description, feature bullets and breadcrumb, as the page states them. Prices are the signed-out online price (null on members-only items). A link that is not a product page fails with an error. Costco answers an unknown product id and a refused browser the same way (HTTP 429, empty page), so both fail with one error that says so.

### How do I automatically get Costco product on costco.com?

Ask an AI agent connected to Reduck to run reduck/costco.com/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/costco.com/get-product

### Is there a costco.com API to get Costco product?

You do not need one. "Get Costco product" drives the real costco.com pages in a browser, so it works whether or not costco.com offers an API for this.

### What information do I need to provide?

Optional: product, product_id.

### What does it return?

It returns url, name, brand, price, rating, currency, features, image_url, breadcrumb, product_id, description, item_number, availability, rating_count.

### Do I need to be logged in to costco.com?

No. It only uses pages of costco.com that are reachable without signing in.

### Does it change anything on costco.com, or only read data?

It only reads. It looks things up on costco.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/costco.com/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/costco.com/get-product

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/costco.com/get-product
