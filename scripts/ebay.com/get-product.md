# Get eBay product

Automatically get eBay product on ebay.com. Fetch one eBay (ebay.com) listing from its item id or link: title, price, currency, availability, condition, brand, images, rating and review count of the catalog product when eBay shows them, the seller with feedback score and positive percentage, the variations of a multi-variation listing, and the catalog product id (epid) to pass to get-product-offers when the listing is tied to one. An id that does not exist or a link that is not a listing fails with an error that says so. No sign-in needed.

- Site: ebay.com
- Address: `reduck/ebay.com/get-product`
- Updated: 2026-11-25 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/ebay.com/get-product`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/ebay.com/get-product
```

## Input

- `product` (string, required): eBay item id (e.g. 366835648867) or listing link (https://www.ebay.com/itm/...), as search-products returns it.

## Output

- `url` (string, required)
- `name` (string | null, required)
- `productId` (string, required): eBay item id.
- `epid` (string | null, optional): eBay catalog product id when the listing is tied to one; pass it to get-product-offers.
- `brand` (string | null, optional)
- `price` (number | null, optional)
- `images` (array, optional)
- `rating` (number | null, optional)
- `seller` (object, optional)
- `currency` (string | null, optional)
- `condition` (string | null, optional)
- `listPrice` (number | null, optional): Struck-through price when eBay shows one.
- `variations` (array, optional): Option menus of a multi-variation listing (size, color...), each with its values; empty otherwise.
- `description` (string | null, optional): Short description from the listing's data, when present.
- `reviewCount` (integer | null, optional)
- `availability` (string | null, optional): schema.org availability, e.g. InStock, OutOfStock.

## FAQ

### What does "Get eBay product" do?

Fetch one eBay (ebay.com) listing from its item id or link: title, price, currency, availability, condition, brand, images, rating and review count of the catalog product when eBay shows them, the seller with feedback score and positive percentage, the variations of a multi-variation listing, and the catalog product id (epid) to pass to get-product-offers when the listing is tied to one. An id that does not exist or a link that is not a listing fails with an error that says so. No sign-in needed.

### How do I automatically get eBay product on ebay.com?

Ask an AI agent connected to Reduck to run reduck/ebay.com/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/ebay.com/get-product

### Is there a ebay.com API to get eBay product?

You do not need one. "Get eBay product" drives the real ebay.com pages in a browser, so it works whether or not ebay.com offers an API for this.

### What information do I need to provide?

Required: product.

### What does it return?

It returns url, epid, name, brand, price, images, rating, seller, currency, condition, listPrice, productId, variations, description, reviewCount, availability.

### Do I need to be logged in to ebay.com?

No. It only uses pages of ebay.com that are reachable without signing in.

### Does it change anything on ebay.com, or only read data?

It only reads. It looks things up on ebay.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/ebay.com/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/ebay.com/get-product

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/ebay.com/get-product
