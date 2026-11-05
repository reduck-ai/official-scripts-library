# Get King Jouet product

Automatically get King Jouet product on king-jouet.com. Read one King Jouet product page from its link: reference, name, brand, price in euros, the availability the page declares, and whether the page offers a button to add it to the cart or to pre-order it. Use it to check one product before adding it with King Jouet add to cart. A link that is not a King Jouet product page fails with an error; a page without a price returns a null price.

- Site: king-jouet.com
- Address: `reduck/king-jouet.com/get_product`
- Updated: 2026-11-04 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/king-jouet.com/get_product`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/king-jouet.com/get_product
```

## Input

- `url` (string, required): Link of a King Jouet product page, as in https://www.king-jouet.com/jeu-jouet/.../ref-1029224-....htm.

## Output

- `ref` (string, required)
- `name` (string | null, required)
- `price` (number | null, required): Price in euros, taxes included.
- `availability` (string | null, required): The availability the page declares, as a schema.org address such as https://schema.org/InStock.
- `can_add_to_cart` (boolean, required): Whether the page shows a button that adds the product to the cart or pre-orders it.
- `brand` (string | null, optional)

## FAQ

### What does "Get King Jouet product" do?

Read one King Jouet product page from its link: reference, name, brand, price in euros, the availability the page declares, and whether the page offers a button to add it to the cart or to pre-order it. Use it to check one product before adding it with King Jouet add to cart. A link that is not a King Jouet product page fails with an error; a page without a price returns a null price.

### How do I automatically get King Jouet product on king-jouet.com?

Ask an AI agent connected to Reduck to run reduck/king-jouet.com/get_product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/king-jouet.com/get_product

### Is there a king-jouet.com API to get King Jouet product?

You do not need one. "Get King Jouet product" drives the real king-jouet.com pages in a browser, so it works whether or not king-jouet.com offers an API for this.

### What information do I need to provide?

Required: url.

### What does it return?

It returns ref, name, brand, price, availability, can_add_to_cart.

### Do I need to be logged in to king-jouet.com?

No. It only uses pages of king-jouet.com that are reachable without signing in.

### Does it change anything on king-jouet.com, or only read data?

It only reads. It looks things up on king-jouet.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/king-jouet.com/get_product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/king-jouet.com/get_product

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/king-jouet.com/get_product
