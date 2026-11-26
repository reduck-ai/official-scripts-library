# Get Leroy Merlin product

Automatically get Leroy Merlin product on leroymerlin.fr. Fetch one leroymerlin.fr product page from its link (as Search Leroy Merlin products returns it). Returns reference, offer id, name, brand, barcode, description, image, price in euros, availability, rating, review count, breadcrumb and the technical characteristics. The price and availability are those the site shows for the browser's current store, or the online price when no store is chosen. A link that is not a product page, or a product that no longer exists, fails with an error that says so.

- Site: leroymerlin.fr
- Address: `reduck/leroymerlin.fr/get-product`
- Updated: 2026-11-24 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/leroymerlin.fr/get-product`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/leroymerlin.fr/get-product
```

## Input

- `url` (string, required): Link of a Leroy Merlin product page, as in https://www.leroymerlin.fr/produits/vis-acier-tete-fraisee-pozidriv-standers-4-x-l-50-mm-82231854.html.

## Output

- `gtin` (string | null, required)
- `name` (string | null, required)
- `brand` (string | null, required)
- `price` (number | null, required)
- `rating` (number | null, required)
- `offerId` (string | null, required): Offer shown on the page, null when the page has no add button.
- `currency` (string | null, required)
- `imageUrl` (string | null, required)
- `productId` (string | null, required)
- `breadcrumb` (array, required)
- `description` (string | null, required)
- `reviewCount` (integer | null, required)
- `availability` (string | null, required): Availability value the site declares, for example OnlineOnly.
- `characteristics` (array, required)

## FAQ

### What does "Get Leroy Merlin product" do?

Fetch one leroymerlin.fr product page from its link (as Search Leroy Merlin products returns it). Returns reference, offer id, name, brand, barcode, description, image, price in euros, availability, rating, review count, breadcrumb and the technical characteristics. The price and availability are those the site shows for the browser's current store, or the online price when no store is chosen. A link that is not a product page, or a product that no longer exists, fails with an error that says so.

### How do I automatically get Leroy Merlin product on leroymerlin.fr?

Ask an AI agent connected to Reduck to run reduck/leroymerlin.fr/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/leroymerlin.fr/get-product

### Is there a leroymerlin.fr API to get Leroy Merlin product?

You do not need one. "Get Leroy Merlin product" drives the real leroymerlin.fr pages in a browser, so it works whether or not leroymerlin.fr offers an API for this.

### What information do I need to provide?

Required: url.

### What does it return?

It returns gtin, name, brand, price, rating, offerId, currency, imageUrl, productId, breadcrumb, description, reviewCount, availability, characteristics.

### Do I need to be logged in to leroymerlin.fr?

No. It only uses pages of leroymerlin.fr that are reachable without signing in.

### Does it change anything on leroymerlin.fr, or only read data?

It only reads. It looks things up on leroymerlin.fr and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/leroymerlin.fr/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/leroymerlin.fr/get-product

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/leroymerlin.fr/get-product
