# Get TopTex product

Automatically get TopTex product on toptex.fr. Fetch a single toptex.fr product by reference (e.g. IB297): name, brand, description, every colorway, every size with its public catalogue unit price, images, fabric/composition and certifications. No login required.

- Site: toptex.fr
- Address: `reduck/toptex.fr/get_product`
- Updated: 2026-08-26 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/toptex.fr/get_product`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/toptex.fr/get_product
```

## Input

- `reference` (string, required): Product reference / supplier code as shown on the PDP and returned by search-products (e.g. "IB297", "CGTW071"). Case-insensitive.

## Output

- `url` (string | null, required)
- `name` (string | null, required)
- `sizes` (array, required): All available sizes with their public catalogue unit price.
- `colors` (array, required): All available colorways.
- `objectID` (string, required)
- `reference` (string, required)
- `brand` (string | null, optional)
- `coupe` (string | null, optional)
- `genre` (string | null, optional)
- `vegan` (string | null, optional)
- `images` (array, optional)
- `modele` (string | null, optional)
- `saison` (array, optional)
- `famille` (string | null, optional)
- `manches` (string | null, optional)
- `oekoTex` (boolean, optional)
- `priceTo` (number | null, optional)
- `typeCol` (string | null, optional)
- `univers` (array, optional)
- `currency` (string, optional)
- `grammage` (integer | null, optional)
- `nbColors` (integer | null, optional)
- `packshots` (array, optional)
- `priceFrom` (number | null, optional)
- `composition` (string | null, optional)
- `description` (string | null, optional)
- `paysOrigine` (string | null, optional)
- `sousFamille` (string | null, optional)

## FAQ

### What does "Get TopTex product" do?

Fetch a single toptex.fr product by reference (e.g. IB297): name, brand, description, every colorway, every size with its public catalogue unit price, images, fabric/composition and certifications. No login required.

### How do I automatically get TopTex product on toptex.fr?

Ask an AI agent connected to Reduck to run reduck/toptex.fr/get_product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/toptex.fr/get_product

### Is there a toptex.fr API to get TopTex product?

You do not need one. "Get TopTex product" drives the real toptex.fr pages in a browser, so it works whether or not toptex.fr offers an API for this.

### What information do I need to provide?

Required: reference.

### What does it return?

It returns url, name, brand, coupe, genre, sizes, vegan, colors, images, modele, saison, famille, manches, oekoTex, priceTo, typeCol, univers, currency, grammage, nbColors, objectID, packshots, priceFrom, reference, composition, description, paysOrigine, sousFamille.

### Do I need to be logged in to toptex.fr?

No. It only uses pages of toptex.fr that are reachable without signing in.

### Does it change anything on toptex.fr, or only read data?

It only reads. It looks things up on toptex.fr and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/toptex.fr/get_product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/toptex.fr/get_product

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/toptex.fr/get_product
