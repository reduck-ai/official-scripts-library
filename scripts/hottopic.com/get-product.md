# Get Hot Topic product

Automatically get Hot Topic product on hottopic.com. Get one Hot Topic (hottopic.com, US) product from its id or its product page link, also the id or link of one of its sizes: product id, link, name, brand, license (the franchise the page names), rating out of 5, price shown and price before the discount in US dollars, whether the price is a starting price, description, category path and images, and every offer (one size or color, or the product itself when it has none) with its offerId, color, size, price in the product data and availability as the site states it (for example InStock, OnlineOnly, PreOrder, OutOfStock). For a product with sizes, the price of an offer is the price before the promotions the cart applies. Pass offerId and the product id to Add a product to the Hot Topic cart. An id or link that Hot Topic does not know fails with a message that says so.

- Site: hottopic.com
- Address: `reduck/hottopic.com/get-product`
- Updated: 2026-11-27 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/hottopic.com/get-product`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/hottopic.com/get-product
```

## Input

- `product` (string, required): Product id (the number at the end of a product link, for example 36930976) or the product link.

## Output

- `id` (string, required): Product id.
- `url` (string, required)
- `name` (string, required)
- `brand` (string | null, required)
- `price` (number | null, required): Price shown, in US dollars.
- `images` (array, required)
- `rating` (number | null, required): Average customer rating out of 5.
- `license` (string | null, required): The franchise or brand line the page links to, for example Sanrio.
- `variants` (array, required)
- `list_price` (number | null, required): Price before the discount, in US dollars, when the page shows one.
- `breadcrumbs` (array, required): Category path of the product.
- `description` (string | null, required)
- `price_is_from` (boolean, required): True when the page shows the price as a starting price.

## FAQ

### What does "Get Hot Topic product" do?

Get one Hot Topic (hottopic.com, US) product from its id or its product page link, also the id or link of one of its sizes: product id, link, name, brand, license (the franchise the page names), rating out of 5, price shown and price before the discount in US dollars, whether the price is a starting price, description, category path and images, and every offer (one size or color, or the product itself when it has none) with its offerId, color, size, price in the product data and availability as the site states it (for example InStock, OnlineOnly, PreOrder, OutOfStock). For a product with sizes, the price of an offer is the price before the promotions the cart applies. Pass offerId and the product id to Add a product to the Hot Topic cart. An id or link that Hot Topic does not know fails with a message that says so.

### How do I automatically get Hot Topic product on hottopic.com?

Ask an AI agent connected to Reduck to run reduck/hottopic.com/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/hottopic.com/get-product

### Is there a hottopic.com API to get Hot Topic product?

You do not need one. "Get Hot Topic product" drives the real hottopic.com pages in a browser, so it works whether or not hottopic.com offers an API for this.

### What information do I need to provide?

Required: product.

### What does it return?

It returns id, url, name, brand, price, images, rating, license, variants, list_price, breadcrumbs, description, price_is_from.

### Do I need to be logged in to hottopic.com?

No. It only uses pages of hottopic.com that are reachable without signing in.

### Does it change anything on hottopic.com, or only read data?

It only reads. It looks things up on hottopic.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/hottopic.com/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/hottopic.com/get-product

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/hottopic.com/get-product
