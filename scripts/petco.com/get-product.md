# Get Petco product

Automatically get Petco product on petco.com. Get one Petco (petco.com, US) product from its id, the item number of one size, or its product page link: product id, link, name, brand, rating out of 5, review count, description, category path, and each size or flavor the page offers with its offerId (item number), name, options (for example weight), price, price before the sale and Repeat Delivery price in US dollars, stock text, units in stock, whether it can be ordered, and whether same day delivery and store pickup are offered. selected_offer_id is the size the link or number names, or the one the page selects. Pass offerId to Add a product to the Petco cart. An id, number or link that Petco does not know fails with a message that says so. Use a managed browser in the US.

- Site: petco.com
- Address: `reduck/petco.com/get-product`
- Updated: 2026-11-27 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/petco.com/get-product`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/petco.com/get-product
```

## Input

- `product` (string, required): Product id (the id a search gives, for example 5030043), the item number of one size (the number at the end of a product link, for example 2998871) or the product link.

## Output

- `id` (string, required): Product id.
- `url` (string, required)
- `name` (string, required)
- `brand` (string | null, required)
- `rating` (number | null, required): Average customer rating out of 5.
- `variants` (array, required): The sizes or flavors of the product.
- `breadcrumbs` (array, required)
- `description` (string | null, required)
- `review_count` (number | null, required)
- `selected_offer_id` (string | null, required): Item number of the size the link or number names, or the one the page selects.

## FAQ

### What does "Get Petco product" do?

Get one Petco (petco.com, US) product from its id, the item number of one size, or its product page link: product id, link, name, brand, rating out of 5, review count, description, category path, and each size or flavor the page offers with its offerId (item number), name, options (for example weight), price, price before the sale and Repeat Delivery price in US dollars, stock text, units in stock, whether it can be ordered, and whether same day delivery and store pickup are offered. selected_offer_id is the size the link or number names, or the one the page selects. Pass offerId to Add a product to the Petco cart. An id, number or link that Petco does not know fails with a message that says so. Use a managed browser in the US.

### How do I automatically get Petco product on petco.com?

Ask an AI agent connected to Reduck to run reduck/petco.com/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/petco.com/get-product

### Is there a petco.com API to get Petco product?

You do not need one. "Get Petco product" drives the real petco.com pages in a browser, so it works whether or not petco.com offers an API for this.

### What information do I need to provide?

Required: product.

### What does it return?

It returns id, url, name, brand, rating, variants, breadcrumbs, description, review_count, selected_offer_id.

### Do I need to be logged in to petco.com?

No. It only uses pages of petco.com that are reachable without signing in.

### Does it change anything on petco.com, or only read data?

It only reads. It looks things up on petco.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/petco.com/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/petco.com/get-product

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/petco.com/get-product
