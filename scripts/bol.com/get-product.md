# Get bol.com product

Automatically get bol.com product on bol.com. Fetch one bol.com product page (Netherlands, Dutch site) by product id or page link: title, link, brand, seller of the best offer, offer id, price in euros and the price for Select members, rating, review count, delivery promise, image link and description, and whether an offer is on sale now. A product with no offer returns available false and no price. An id or link that is not a bol.com product fails with an error that says so.

- Site: bol.com
- Address: `reduck/bol.com/get-product`
- Updated: 2026-11-24 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/bol.com/get-product`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/bol.com/get-product
```

## Input

- `product` (string, required): A bol.com product id as returned by Search bol.com products (for example 9300000000353594), or the link of a bol.com product page.

## Output

- `url` (string | null, required)
- `brand` (string | null, required)
- `price` (number | null, required)
- `title` (string | null, required)
- `rating` (number | null, required)
- `seller` (string | null, required)
- `offerId` (string | null, required)
- `currency` (string | null, required)
- `imageUrl` (string | null, required)
- `available` (boolean, required)
- `productId` (string, required)
- `description` (string | null, required)
- `reviewCount` (integer | null, required)
- `selectPrice` (number | null, required)
- `deliveryDescription` (string | null, required)

## FAQ

### What does "Get bol.com product" do?

Fetch one bol.com product page (Netherlands, Dutch site) by product id or page link: title, link, brand, seller of the best offer, offer id, price in euros and the price for Select members, rating, review count, delivery promise, image link and description, and whether an offer is on sale now. A product with no offer returns available false and no price. An id or link that is not a bol.com product fails with an error that says so.

### How do I automatically get bol.com product on bol.com?

Ask an AI agent connected to Reduck to run reduck/bol.com/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/bol.com/get-product

### Is there a bol.com API to get bol.com product?

You do not need one. "Get bol.com product" drives the real bol.com pages in a browser, so it works whether or not bol.com offers an API for this.

### What information do I need to provide?

Required: product.

### What does it return?

It returns url, brand, price, title, rating, seller, offerId, currency, imageUrl, available, productId, description, reviewCount, selectPrice, deliveryDescription.

### Do I need to be logged in to bol.com?

No. It only uses pages of bol.com that are reachable without signing in.

### Does it change anything on bol.com, or only read data?

It only reads. It looks things up on bol.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/bol.com/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/bol.com/get-product

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/bol.com/get-product
