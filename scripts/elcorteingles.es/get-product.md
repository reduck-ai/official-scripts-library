# Get El Corte Inglés product

Automatically get El Corte Inglés product on elcorteingles.es. Fetch one El Corte Inglés Spain (elcorteingles.es) product page by product id or product link. Returns title, link, brand, barcode number, price and struck-through price in euros, discount, main image and all images, status, seller (El Corte Inglés or a marketplace seller), category path, description, technical data, every colour and size with its own reference, price and status, and the offers of the marketplace sellers when the page lists them. Texts are in Spanish. An unknown product id fails with an error that says so. Ratings are not returned: the site does not give them with the product data.

- Site: elcorteingles.es
- Address: `reduck/elcorteingles.es/get-product`
- Updated: 2026-11-24 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/elcorteingles.es/get-product`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/elcorteingles.es/get-product
```

## Input

- `product` (string, required): El Corte Inglés product id (the product_id of Search El Corte Inglés products, for example A54773733 or MP_0470146_8004399334601), or the product link itself.

## Output

- `url` (string | null, required)
- `price` (number | null, required): Price in euros, VAT included, of the colour and size the page shows first.
- `title` (string | null, required)
- `offers` (array, required): The marketplace sellers that offer the version the page shows first, each with its price. Empty when El Corte Inglés sells it alone.
- `seller` (string | null, required): El Corte Inglés, or the name of the marketplace seller.
- `variants` (array, required): Every colour and size of the product, each with its own reference. One entry when the product has a single version.
- `requested` (string, required): The product argument as given.
- `product_id` (string, required)
- `ean` (string | null, optional): EAN barcode of the colour and size the page shows first.
- `brand` (string | null, optional)
- `images` (array, optional): Images of the colour the page shows first.
- `image_url` (string | null, optional)
- `breadcrumb` (array, optional): Category path, in Spanish.
- `list_price` (number | null, optional): Struck-through price in euros, null when none is shown.
- `description` (string | null, optional): Product description as plain text.
- `marketplace` (boolean | null, optional)
- `availability` (string | null, optional): Status as El Corte Inglés codes it, for example ADD (can be bought).
- `specifications` (array, optional): Technical data as the site lists it, in Spanish.
- `discount_percentage` (number | null, optional)

## FAQ

### What does "Get El Corte Inglés product" do?

Fetch one El Corte Inglés Spain (elcorteingles.es) product page by product id or product link. Returns title, link, brand, barcode number, price and struck-through price in euros, discount, main image and all images, status, seller (El Corte Inglés or a marketplace seller), category path, description, technical data, every colour and size with its own reference, price and status, and the offers of the marketplace sellers when the page lists them. Texts are in Spanish. An unknown product id fails with an error that says so. Ratings are not returned: the site does not give them with the product data.

### How do I automatically get El Corte Inglés product on elcorteingles.es?

Ask an AI agent connected to Reduck to run reduck/elcorteingles.es/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/elcorteingles.es/get-product

### Is there a elcorteingles.es API to get El Corte Inglés product?

You do not need one. "Get El Corte Inglés product" drives the real elcorteingles.es pages in a browser, so it works whether or not elcorteingles.es offers an API for this.

### What information do I need to provide?

Required: product.

### What does it return?

It returns ean, url, brand, price, title, images, offers, seller, variants, image_url, requested, breadcrumb, list_price, product_id, description, marketplace, availability, specifications, discount_percentage.

### Do I need to be logged in to elcorteingles.es?

No. It only uses pages of elcorteingles.es that are reachable without signing in.

### Does it change anything on elcorteingles.es, or only read data?

It only reads. It looks things up on elcorteingles.es and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/elcorteingles.es/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/elcorteingles.es/get-product

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/elcorteingles.es/get-product
