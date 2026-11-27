# Get Micromania product

Automatically get Micromania product on micromania.fr. Fetch one Micromania.fr product page from its link (the url that Search Micromania products returns). Returns sku, title, brand, ean, price and struck-through list_price in euros, rating, review_count, availability, condition, seller, release date, description, breadcrumb, images and whether the product can be added to the cart. A link that is not a product page, or a product that no longer exists, fails with an error that says so.

- Site: micromania.fr
- Address: `reduck/micromania.fr/get-product`
- Updated: 2026-11-24 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/micromania.fr/get-product`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/micromania.fr/get-product
```

## Input

- `url` (string, required): Link of a Micromania product page, as Search Micromania products returns it in url, such as https://www.micromania.fr/p/booster-pokemon-mega-brave-ou-mega-symphonia-japonais-152771.html.

## Output

- `ean` (string | null, required)
- `sku` (string, required): Micromania product id.
- `url` (string | null, required)
- `brand` (string | null, required)
- `price` (number | null, required): Price in euros.
- `title` (string | null, required)
- `images` (array, required)
- `rating` (number | null, required)
- `seller` (string | null, required)
- `currency` (string | null, required)
- `condition` (string | null, required): Condition the site declares, such as NewCondition.
- `breadcrumb` (array, required)
- `list_price` (number | null, required): Struck-through price in euros, when the site shows one.
- `description` (string | null, required)
- `availability` (string | null, required): Availability the site declares, such as InStock.
- `release_date` (string | null, required): Release date as the page states it.
- `review_count` (integer | null, required)
- `can_add_to_cart` (boolean, required)

## FAQ

### What does "Get Micromania product" do?

Fetch one Micromania.fr product page from its link (the url that Search Micromania products returns). Returns sku, title, brand, ean, price and struck-through list_price in euros, rating, review_count, availability, condition, seller, release date, description, breadcrumb, images and whether the product can be added to the cart. A link that is not a product page, or a product that no longer exists, fails with an error that says so.

### How do I automatically get Micromania product on micromania.fr?

Ask an AI agent connected to Reduck to run reduck/micromania.fr/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/micromania.fr/get-product

### Is there a micromania.fr API to get Micromania product?

You do not need one. "Get Micromania product" drives the real micromania.fr pages in a browser, so it works whether or not micromania.fr offers an API for this.

### What information do I need to provide?

Required: url.

### What does it return?

It returns ean, sku, url, brand, price, title, images, rating, seller, currency, condition, breadcrumb, list_price, description, availability, release_date, review_count, can_add_to_cart.

### Do I need to be logged in to micromania.fr?

No. It only uses pages of micromania.fr that are reachable without signing in.

### Does it change anything on micromania.fr, or only read data?

It only reads. It looks things up on micromania.fr and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/micromania.fr/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/micromania.fr/get-product

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/micromania.fr/get-product
