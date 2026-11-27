# Get a CVS product

Automatically get a CVS product on cvs.com. Get one CVS product (cvs.com, US) from its id or its page link: name, link, brand, category, price, currency, availability, rating, review count, images, and its variants (size, count, color and so on) with their ids for add_to_cart, prices, deal and the most the site sells per order. An id the site does not know, or a link that is not a product page, gives an error that says so. CVS sometimes shows its Access Denied page to managed browsers, mostly when several open at the same time: the script then fails with an error that says so, and a later retry often works.

- Site: cvs.com
- Address: `reduck/cvs.com/get-product`
- Updated: 2026-11-26 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/cvs.com/get-product`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/cvs.com/get-product
```

## Input

- `product` (string, required): The product id (e.g. "1010742", from search-products) or the link of its page on cvs.com.

## Output

- `id` (string, required)
- `name` (string, required)
- `variants` (array, required): The variants the site sells the product in. Pass an id as variantId to add_to_cart.
- `url` (string | null, optional)
- `brand` (string | null, optional)
- `price` (number | null, optional): The price the page shows, in the currency below.
- `images` (array, optional)
- `rating` (number | null, optional): The average rating out of 5, or null with no review.
- `category` (string | null, optional): The category path the site gives, e.g. "Vitamins > Letter Vitamins > Vitamin C".
- `currency` (string | null, optional)
- `availability` (string | null, optional): The availability the site states, e.g. InStock.
- `review_count` (integer | null, optional)

## FAQ

### What does "Get a CVS product" do?

Get one CVS product (cvs.com, US) from its id or its page link: name, link, brand, category, price, currency, availability, rating, review count, images, and its variants (size, count, color and so on) with their ids for add_to_cart, prices, deal and the most the site sells per order. An id the site does not know, or a link that is not a product page, gives an error that says so. CVS sometimes shows its Access Denied page to managed browsers, mostly when several open at the same time: the script then fails with an error that says so, and a later retry often works.

### How do I automatically get a CVS product on cvs.com?

Ask an AI agent connected to Reduck to run reduck/cvs.com/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/cvs.com/get-product

### Is there a cvs.com API to get a CVS product?

You do not need one. "Get a CVS product" drives the real cvs.com pages in a browser, so it works whether or not cvs.com offers an API for this.

### What information do I need to provide?

Required: product.

### What does it return?

It returns id, url, name, brand, price, images, rating, category, currency, variants, availability, review_count.

### Do I need to be logged in to cvs.com?

No. It only uses pages of cvs.com that are reachable without signing in.

### Does it change anything on cvs.com, or only read data?

It only reads. It looks things up on cvs.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/cvs.com/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/cvs.com/get-product

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/cvs.com/get-product
