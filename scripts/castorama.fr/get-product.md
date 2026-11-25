# Get Castorama product

Automatically get Castorama product on castorama.fr. Fetch one castorama.fr product page by its link or its product id (from Search Castorama products). Returns the name, price and struck-through list price in euros, rating and review count, the seller (Castorama or a partner seller), availability and purchasable flag, delivery and pick-up availability, description, highlights, the technical specifications, the images and the breadcrumb. Prices are those shown to this browser, which can depend on the store or postcode chosen on the site. An unknown id or a link that is not a product page fails with an error that says so.

- Site: castorama.fr
- Address: `reduck/castorama.fr/get-product`
- Updated: 2026-11-24 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/castorama.fr/get-product`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/castorama.fr/get-product
```

## Input

- `product` (string, required): A castorama.fr product link (ends with <id>_CAFR.prd) or the product id returned by Search Castorama products, for example 5063022700711.

## Output

- `url` (string | null, required)
- `name` (string | null, required)
- `productId` (string, required)
- `price` (number | null, optional): Current price in euros, taxes included.
- `images` (array, optional)
- `rating` (number | null, optional)
- `seller` (string | null, optional)
- `status` (string | null, optional)
- `offerId` (string | null, optional)
- `currency` (string | null, optional)
- `features` (array, optional)
- `listPrice` (number | null, optional): Struck-through price in euros, when the product is discounted.
- `breadcrumb` (array, optional)
- `fulfilment` (object, optional)
- `sellerType` (string | null, optional)
- `description` (string | null, optional)
- `purchasable` (boolean | null, optional)
- `reviewCount` (integer | null, optional)
- `specifications` (array, optional)

## FAQ

### What does "Get Castorama product" do?

Fetch one castorama.fr product page by its link or its product id (from Search Castorama products). Returns the name, price and struck-through list price in euros, rating and review count, the seller (Castorama or a partner seller), availability and purchasable flag, delivery and pick-up availability, description, highlights, the technical specifications, the images and the breadcrumb. Prices are those shown to this browser, which can depend on the store or postcode chosen on the site. An unknown id or a link that is not a product page fails with an error that says so.

### How do I automatically get Castorama product on castorama.fr?

Ask an AI agent connected to Reduck to run reduck/castorama.fr/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/castorama.fr/get-product

### Is there a castorama.fr API to get Castorama product?

You do not need one. "Get Castorama product" drives the real castorama.fr pages in a browser, so it works whether or not castorama.fr offers an API for this.

### What information do I need to provide?

Required: product.

### What does it return?

It returns url, name, price, images, rating, seller, status, offerId, currency, features, listPrice, productId, breadcrumb, fulfilment, sellerType, description, purchasable, reviewCount, specifications.

### Do I need to be logged in to castorama.fr?

No. It only uses pages of castorama.fr that are reachable without signing in.

### Does it change anything on castorama.fr, or only read data?

It only reads. It looks things up on castorama.fr and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/castorama.fr/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/castorama.fr/get-product

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/castorama.fr/get-product
