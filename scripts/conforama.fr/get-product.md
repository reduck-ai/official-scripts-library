# Get Conforama product

Automatically get Conforama product on conforama.fr. Fetch one Conforama.fr product page by its product id (for example 769466) or its page link, both returned by Search Conforama products. Returns name, EAN, price and struck-through list price in euros, eco-participation, availability, condition, rating and review count, the seller, description, images, breadcrumb and the main characteristics. A link that is not a Conforama product page fails with an error that says so.

- Site: conforama.fr
- Address: `reduck/conforama.fr/get-product`
- Updated: 2026-11-24 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/conforama.fr/get-product`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/conforama.fr/get-product
```

## Input

- `product` (string, required): Product id such as 769466 (marketplace ids look like M76822802), or the link of the Conforama product page, as returned by Search Conforama products.

## Output

- `url` (string, required)
- `name` (string, required)
- `product_id` (string, required)
- `gtin` (string | null, optional): EAN barcode.
- `price` (number | null, optional): Current price in euros.
- `images` (array, optional)
- `rating` (number | null, optional)
- `seller` (string | null, optional)
- `currency` (string | null, optional)
- `eco_part` (number | null, optional): Eco-participation in euros, already included in the price.
- `features` (array, optional)
- `condition` (string | null, optional)
- `breadcrumb` (array, optional)
- `list_price` (number | null, optional): Struck-through price in euros when the product is discounted.
- `description` (string | null, optional)
- `availability` (string | null, optional): Availability as the site declares it, such as InStock.
- `review_count` (integer | null, optional)

## FAQ

### What does "Get Conforama product" do?

Fetch one Conforama.fr product page by its product id (for example 769466) or its page link, both returned by Search Conforama products. Returns name, EAN, price and struck-through list price in euros, eco-participation, availability, condition, rating and review count, the seller, description, images, breadcrumb and the main characteristics. A link that is not a Conforama product page fails with an error that says so.

### How do I automatically get Conforama product on conforama.fr?

Ask an AI agent connected to Reduck to run reduck/conforama.fr/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/conforama.fr/get-product

### Is there a conforama.fr API to get Conforama product?

You do not need one. "Get Conforama product" drives the real conforama.fr pages in a browser, so it works whether or not conforama.fr offers an API for this.

### What information do I need to provide?

Required: product.

### What does it return?

It returns url, gtin, name, price, images, rating, seller, currency, eco_part, features, condition, breadcrumb, list_price, product_id, description, availability, review_count.

### Do I need to be logged in to conforama.fr?

No. It only uses pages of conforama.fr that are reachable without signing in.

### Does it change anything on conforama.fr, or only read data?

It only reads. It looks things up on conforama.fr and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/conforama.fr/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/conforama.fr/get-product

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/conforama.fr/get-product
