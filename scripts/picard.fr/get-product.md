# Get a Picard product

Automatically get a Picard product on picard.fr. Read one product of the Picard France store (picard.fr, frozen food) from its product id or its link: name, reference, packaging, price in euros, price per kilo or per unit, description, images, rating and review count, Nutri-Score and Planet-Score, origin, the breadcrumb of categories, and whether the product can be added to the cart online. The price is the national price of the French web store, as shown to a guest who has not chosen a delivery postcode or a store. An id or link that the store does not have fails with a message that says so.

- Site: picard.fr
- Address: `reduck/picard.fr/get-product`
- Updated: 2026-11-26 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/picard.fr/get-product`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/picard.fr/get-product
```

## Input

- `product` (string, required): The product id from Search Picard products (for example "000000000000083390", leading zeros optional) or a picard.fr product link.

## Output

- `url` (string, required)
- `name` (string | null, required)
- `productId` (string, required)
- `price` (number | null, optional): Price in euros.
- `images` (array, optional)
- `origin` (string | null, optional)
- `rating` (number | null, optional): Average rating out of 5.
- `currency` (string | null, optional)
- `packaging` (string | null, optional)
- `reference` (string | null, optional): The short reference the site shows (for example "083390").
- `breadcrumb` (array, optional): The categories of the product page, from the home page to the product, as the site lists them.
- `nutriscore` (string | null, optional)
- `description` (string | null, optional)
- `planetscore` (string | null, optional)
- `reviewCount` (integer | null, optional)
- `availability` (string | null, optional): Availability as the site states it, if it does.
- `canAddToCart` (boolean, optional): True when the page offers to add the product to the cart online.
- `pricePerUnit` (string | null, optional): Price per kilo, per litre or per piece, as the site writes it.

## FAQ

### What does "Get a Picard product" do?

Read one product of the Picard France store (picard.fr, frozen food) from its product id or its link: name, reference, packaging, price in euros, price per kilo or per unit, description, images, rating and review count, Nutri-Score and Planet-Score, origin, the breadcrumb of categories, and whether the product can be added to the cart online. The price is the national price of the French web store, as shown to a guest who has not chosen a delivery postcode or a store. An id or link that the store does not have fails with a message that says so.

### How do I automatically get a Picard product on picard.fr?

Ask an AI agent connected to Reduck to run reduck/picard.fr/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/picard.fr/get-product

### Is there a picard.fr API to get a Picard product?

You do not need one. "Get a Picard product" drives the real picard.fr pages in a browser, so it works whether or not picard.fr offers an API for this.

### What information do I need to provide?

Required: product.

### What does it return?

It returns url, name, price, images, origin, rating, currency, packaging, productId, reference, breadcrumb, nutriscore, description, planetscore, reviewCount, availability, canAddToCart, pricePerUnit.

### Do I need to be logged in to picard.fr?

No. It only uses pages of picard.fr that are reachable without signing in.

### Does it change anything on picard.fr, or only read data?

It only reads. It looks things up on picard.fr and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/picard.fr/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/picard.fr/get-product

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/picard.fr/get-product
