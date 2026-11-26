# Get Etsy product

Automatically get Etsy product on etsy.com. Fetch one Etsy (etsy.com) listing from its id or link: title, description, images, price and original price when on sale, currency, availability, rating and review count, shop, category, where it ships from, and its option menus (size, color...) with each option's label, id and whether it is sold out, as add_to_cart takes them. Each Etsy listing is sold by one shop. A listing that does not exist or a link that is not a listing fails with an error that says so.

- Site: etsy.com
- Address: `reduck/etsy.com/get-product`
- Updated: 2026-11-25 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/etsy.com/get-product`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/etsy.com/get-product
```

## Input

- `product` (string, required): Etsy listing id (e.g. 4571868333) or listing link (https://www.etsy.com/listing/...), as search-products returns it.

## Output

- `url` (string, required)
- `name` (string | null, required)
- `productId` (string, required)
- `price` (number | null, optional)
- `images` (array, optional)
- `rating` (number | null, optional)
- `seller` (string | null, optional): Shop name.
- `category` (array, optional)
- `currency` (string | null, optional)
- `listPrice` (number | null, optional): Original price when on sale.
- `sellerUrl` (string | null, optional)
- `shipsFrom` (string | null, optional): Country code the shop ships from.
- `variations` (array, optional): Option menus; pass one label per menu, in order, as add_to_cart's options.
- `description` (string | null, optional)
- `reviewCount` (integer | null, optional)
- `availability` (string | null, optional): schema.org availability, e.g. InStock.

## FAQ

### What does "Get Etsy product" do?

Fetch one Etsy (etsy.com) listing from its id or link: title, description, images, price and original price when on sale, currency, availability, rating and review count, shop, category, where it ships from, and its option menus (size, color...) with each option's label, id and whether it is sold out, as add_to_cart takes them. Each Etsy listing is sold by one shop. A listing that does not exist or a link that is not a listing fails with an error that says so.

### How do I automatically get Etsy product on etsy.com?

Ask an AI agent connected to Reduck to run reduck/etsy.com/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/etsy.com/get-product

### Is there a etsy.com API to get Etsy product?

You do not need one. "Get Etsy product" drives the real etsy.com pages in a browser, so it works whether or not etsy.com offers an API for this.

### What information do I need to provide?

Required: product.

### What does it return?

It returns url, name, price, images, rating, seller, category, currency, listPrice, productId, sellerUrl, shipsFrom, variations, description, reviewCount, availability.

### Do I need to be logged in to etsy.com?

No. It only uses pages of etsy.com that are reachable without signing in.

### Does it change anything on etsy.com, or only read data?

It only reads. It looks things up on etsy.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/etsy.com/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/etsy.com/get-product

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/etsy.com/get-product
