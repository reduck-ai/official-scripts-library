# Get Rue du Commerce product

Automatically get Rue du Commerce product on rueducommerce.fr. Reads a rueducommerce.fr product page from its link or product id and returns its name, brand, price in euros, seller, availability, condition, images, categories and the offer id used to add it to the cart. A link that is not a product page is refused.

- Site: rueducommerce.fr
- Address: `reduck/rueducommerce.fr/get-product`
- Updated: 2026-11-24 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/rueducommerce.fr/get-product`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/rueducommerce.fr/get-product
```

## Input

- `product` (string, required): A www.rueducommerce.fr/p/<id>.html link, or the product id from search-products (for example r25109147605).

## Output

- `url` (string, required)
- `name` (string | null, required)
- `price` (number | null, required)
- `offerId` (string | null, required): Offer id to pass to add_to_cart. Null when the page has no add-to-cart button.
- `productId` (string, required)
- `mpn` (string | null, optional)
- `sku` (string | null, optional)
- `gtin` (string | null, optional)
- `brand` (string | null, optional)
- `seller` (string | null, optional)
- `currency` (string | null, optional)
- `condition` (string | null, optional)
- `imageUrls` (array, optional)
- `categories` (array, optional)
- `description` (string | null, optional)
- `availability` (string | null, optional): Schema.org availability, for example InStock or OutOfStock.
- `isMarketplace` (boolean | null, optional)

## FAQ

### What does "Get Rue du Commerce product" do?

Reads a rueducommerce.fr product page from its link or product id and returns its name, brand, price in euros, seller, availability, condition, images, categories and the offer id used to add it to the cart. A link that is not a product page is refused.

### How do I automatically get Rue du Commerce product on rueducommerce.fr?

Ask an AI agent connected to Reduck to run reduck/rueducommerce.fr/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/rueducommerce.fr/get-product

### Is there a rueducommerce.fr API to get Rue du Commerce product?

You do not need one. "Get Rue du Commerce product" drives the real rueducommerce.fr pages in a browser, so it works whether or not rueducommerce.fr offers an API for this.

### What information do I need to provide?

Required: product.

### What does it return?

It returns mpn, sku, url, gtin, name, brand, price, seller, offerId, currency, condition, imageUrls, productId, categories, description, availability, isMarketplace.

### Do I need to be logged in to rueducommerce.fr?

No. It only uses pages of rueducommerce.fr that are reachable without signing in.

### Does it change anything on rueducommerce.fr, or only read data?

It only reads. It looks things up on rueducommerce.fr and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/rueducommerce.fr/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/rueducommerce.fr/get-product

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/rueducommerce.fr/get-product
