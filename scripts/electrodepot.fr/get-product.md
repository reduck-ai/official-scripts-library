# Get Electro Dépôt product

Automatically get Electro Dépôt product on electrodepot.fr. Read one product of the Electro Dépôt French store (electrodepot.fr) from its product id or its product page link: reference, name, link, brand, price and former price in euros (taxes included), eco-participation, condition, categories, images, description text, the specification table, and availability: home delivery, the delivery fee, and pickup at the store the site chose for this browser (its city, now or later, and in how many days). The site picks that store from where the browser connects; when it has chosen none, as for most new guests, the store fields are null. A product id or link that the site does not know fails with an error that says so. Get product ids from Search Electro Dépôt products.

- Site: electrodepot.fr
- Address: `reduck/electrodepot.fr/get-product`
- Updated: 2026-11-27 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/electrodepot.fr/get-product`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/electrodepot.fr/get-product
```

## Input

- `product` (string, required): Product id from Search Electro Dépôt products (for example 36453), or a product page link such as https://www.electrodepot.fr/casque-bluetooth-edenwood-supra-b01.html.

## Output

- `url` (string | null, required)
- `name` (string | null, required)
- `brand` (string | null, required)
- `price` (number | null, required): Price in euros, taxes included.
- `images` (array, required)
- `currency` (string, required)
- `condition` (string | null, required): Condition as the site gives it, for example neuf.
- `productId` (string, required)
- `reference` (string | null, required): The product reference the site shows.
- `categories` (array, required)
- `description` (string | null, required)
- `formerPrice` (number | null, required): Struck-through former price in euros, when the site shows one.
- `availability` (object | null, required)
- `specifications` (array, required)
- `ecoParticipation` (number | null, required): Eco-participation in euros, included in the price.

## FAQ

### What does "Get Electro Dépôt product" do?

Read one product of the Electro Dépôt French store (electrodepot.fr) from its product id or its product page link: reference, name, link, brand, price and former price in euros (taxes included), eco-participation, condition, categories, images, description text, the specification table, and availability: home delivery, the delivery fee, and pickup at the store the site chose for this browser (its city, now or later, and in how many days). The site picks that store from where the browser connects; when it has chosen none, as for most new guests, the store fields are null. A product id or link that the site does not know fails with an error that says so. Get product ids from Search Electro Dépôt products.

### How do I automatically get Electro Dépôt product on electrodepot.fr?

Ask an AI agent connected to Reduck to run reduck/electrodepot.fr/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/electrodepot.fr/get-product

### Is there a electrodepot.fr API to get Electro Dépôt product?

You do not need one. "Get Electro Dépôt product" drives the real electrodepot.fr pages in a browser, so it works whether or not electrodepot.fr offers an API for this.

### What information do I need to provide?

Required: product.

### What does it return?

It returns url, name, brand, price, images, currency, condition, productId, reference, categories, description, formerPrice, availability, specifications, ecoParticipation.

### Do I need to be logged in to electrodepot.fr?

No. It only uses pages of electrodepot.fr that are reachable without signing in.

### Does it change anything on electrodepot.fr, or only read data?

It only reads. It looks things up on electrodepot.fr and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/electrodepot.fr/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/electrodepot.fr/get-product

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/electrodepot.fr/get-product
