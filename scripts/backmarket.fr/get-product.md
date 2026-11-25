# Get Back Market France product

Automatically get Back Market France product on backmarket.fr. Fetch one backmarket.fr product page from its link (as Search Back Market France products returns it, the grade is the l parameter). Returns the title, brand, model, color, type (new or refurbished), the price when new, and the offer the page shows for that grade: offer id, price in euros, condition grade, seller (name, country, city, seller since), warranty, delivery dates and whether delivery is free. Also returns the grade and variant choices the page offers and whether the product is out of stock. A link that is not a product page fails with an error.

- Site: backmarket.fr
- Address: `reduck/backmarket.fr/get-product`
- Updated: 2026-11-24 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/backmarket.fr/get-product`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/backmarket.fr/get-product
```

## Input

- `link` (string, required): Product page link on www.backmarket.fr, from Search Back Market France products, e.g. https://www.backmarket.fr/fr-fr/p/<name>/<id>?l=10

## Output

- `url` (string, required)
- `images` (array, required)
- `choices` (array, required): The grade and variant pickers of the page, as the site gives them.
- `productId` (string, required)
- `brand` (string | null, optional)
- `color` (string | null, optional)
- `model` (string | null, optional)
- `offer` (object | null, optional)
- `title` (string | null, optional)
- `category` (string | null, optional)
- `currency` (string | null, optional)
- `description` (string | null, optional)
- `productType` (string | null, optional)
- `isOutOfStock` (boolean | null, optional)
- `priceWhenNew` (number | null, optional)

## FAQ

### What does "Get Back Market France product" do?

Fetch one backmarket.fr product page from its link (as Search Back Market France products returns it, the grade is the l parameter). Returns the title, brand, model, color, type (new or refurbished), the price when new, and the offer the page shows for that grade: offer id, price in euros, condition grade, seller (name, country, city, seller since), warranty, delivery dates and whether delivery is free. Also returns the grade and variant choices the page offers and whether the product is out of stock. A link that is not a product page fails with an error.

### How do I automatically get Back Market France product on backmarket.fr?

Ask an AI agent connected to Reduck to run reduck/backmarket.fr/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/backmarket.fr/get-product

### Is there a backmarket.fr API to get Back Market France product?

You do not need one. "Get Back Market France product" drives the real backmarket.fr pages in a browser, so it works whether or not backmarket.fr offers an API for this.

### What information do I need to provide?

Required: link.

### What does it return?

It returns url, brand, color, model, offer, title, images, choices, category, currency, productId, description, productType, isOutOfStock, priceWhenNew.

### Do I need to be logged in to backmarket.fr?

No. It only uses pages of backmarket.fr that are reachable without signing in.

### Does it change anything on backmarket.fr, or only read data?

It only reads. It looks things up on backmarket.fr and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/backmarket.fr/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/backmarket.fr/get-product

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/backmarket.fr/get-product
