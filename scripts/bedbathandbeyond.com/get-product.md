# Get a Bed Bath & Beyond product

Automatically get a Bed Bath & Beyond product on bedbathandbeyond.com. Get one Bed Bath & Beyond product from its id or its page link: name, link, price, comparison price, currency, availability, rating, review count, images, brand, and its options (color, size and so on) with their ids for add_to_cart. An id the site does not know, or a link that is not a product page, gives an error that says so.

- Site: bedbathandbeyond.com
- Address: `reduck/bedbathandbeyond.com/get-product`
- Updated: 2026-11-26 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/bedbathandbeyond.com/get-product`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/bedbathandbeyond.com/get-product
```

## Input

- `product` (string, required): The product id (e.g. "43932864", from search-products) or the link of its page on bedbathandbeyond.com.

## Output

- `id` (string, required)
- `name` (string, required)
- `url` (string | null, optional)
- `brand` (string | null, optional)
- `price` (number | null, optional): The lowest current price among the options.
- `images` (array, optional)
- `rating` (number | null, optional): The average rating out of 5, or null with no review.
- `currency` (string | null, optional)
- `variants` (array, optional): The options the site sells the product in. Pass an id as optionId to add_to_cart.
- `list_price` (number | null, optional): The comparison price (MSRP or was price) of that option, or null.
- `availability` (string | null, optional): InStock or OutOfStock, as the site states it.
- `review_count` (integer | null, optional)

## FAQ

### What does "Get a Bed Bath & Beyond product" do?

Get one Bed Bath & Beyond product from its id or its page link: name, link, price, comparison price, currency, availability, rating, review count, images, brand, and its options (color, size and so on) with their ids for add_to_cart. An id the site does not know, or a link that is not a product page, gives an error that says so.

### How do I automatically get a Bed Bath & Beyond product on bedbathandbeyond.com?

Ask an AI agent connected to Reduck to run reduck/bedbathandbeyond.com/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/bedbathandbeyond.com/get-product

### Is there a bedbathandbeyond.com API to get a Bed Bath & Beyond product?

You do not need one. "Get a Bed Bath & Beyond product" drives the real bedbathandbeyond.com pages in a browser, so it works whether or not bedbathandbeyond.com offers an API for this.

### What information do I need to provide?

Required: product.

### What does it return?

It returns id, url, name, brand, price, images, rating, currency, variants, list_price, availability, review_count.

### Do I need to be logged in to bedbathandbeyond.com?

No. It only uses pages of bedbathandbeyond.com that are reachable without signing in.

### Does it change anything on bedbathandbeyond.com, or only read data?

It only reads. It looks things up on bedbathandbeyond.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/bedbathandbeyond.com/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/bedbathandbeyond.com/get-product

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/bedbathandbeyond.com/get-product
