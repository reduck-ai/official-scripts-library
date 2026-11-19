# Get Amazon.fr product

Automatically get Amazon.fr product on amazon.fr. Fetch a single Amazon.fr product page by ASIN. Returns title, byline, brand, price, list_price, rating, review_count, rating_breakdown, availability, breadcrumb, image_url, feature_bullets, description, attributes, variant_asins, deal, badges, delivery_estimate, return_policy, and seller. deal is the deal the page shows: its id, its label as Amazon writes it (for example "Offre Pré-Black Friday") and its end time. badges are the other badges next to the title, for example Choix d'Amazon. The returned asin can differ from the requested one when Amazon resolves a variant. For books, brand is null and feature_bullets and attributes are usually empty. Audible audiobook ASINs open Audible's own product page instead, so they fail at once with an error that gives that page's URL.

- Site: amazon.fr
- Address: `reduck/amazon.fr/get-product`
- Updated: 2026-11-18 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/amazon.fr/get-product`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/amazon.fr/get-product
```

## Input

- `asin` (string, required)
- `zipCode` (string, optional)

## Output

- `url` (string, required): Canonical URL the page declares. Usually /dp/<asin>; some Amazon-brand products declare a /clp/<asin> URL instead.
- `zip` (string, required): French postcode the store was pinned to for this fetch.
- `asin` (string | null, required): ASIN actually displayed (differs from requested when Amazon resolves a variant).
- `deal` (object | null, required): The deal that the page shows for this product. Null when there is no deal. A deal can apply to one variant only: then only the ASIN of that variant shows it.
- `brand` (string | null, required): Brand parsed from the byline. Null for books, whose byline names authors instead.
- `price` (object | null, required): Featured-offer price as {value, currency}. Null when no buy-now price shows (e.g. a Kindle title not available for purchase). {raw,value:null} when a currency symbol couldn't be parsed.
- `title` (string | null, required)
- `badges` (array, required): Badges next to the title, other than the deal. Empty when there are none.
- `byline` (string | null, required): Verbatim byline — e.g. "Visit the Anker Store", "by Author (Author)".
- `rating` (number | null, required): Average stars out of 5.
- `seller` (object | null, required): Sold-by seller {name, id}, e.g. {name: "Amazon.fr", id: null}; id is null for Amazon Retail / when no seller link is shown. Both null when the page shows no seller.
- `image_url` (string | null, required): Main product image (high-res when available).
- `attributes` (object, required): Product-overview spec table; empty when not rendered.
- `breadcrumb` (array, required): Category path; empty when no wayfinding breadcrumb (e.g. Amazon devices).
- `list_price` (object | null, required): Struck-through list price as {value, currency}, when shown.
- `description` (string | null, required): Product description block, when present.
- `availability` (string | null, required): Visible availability message — "In Stock", "Only N left", or the unshippable message.
- `review_count` (integer | null, required)
- `return_policy` (string | null, required): Return policy summary, e.g. "FREE Returns".
- `variant_asins` (array, required): Sibling variant ASINs from the variation widget; empty when the product has no variations.
- `requested_asin` (string, required): ASIN passed in by the caller — the join key.
- `feature_bullets` (array, required): "About this item" bullets; empty when not rendered (e.g. books).
- `rating_breakdown` (object | null, required): Percentage of ratings per star bucket, e.g. {"5_star":"73%"}. Null when not rendered.
- `delivery_estimate` (string | null, required): Delivery date/time message, when shown.

## FAQ

### What does "Get Amazon.fr product" do?

Fetch a single Amazon.fr product page by ASIN. Returns title, byline, brand, price, list_price, rating, review_count, rating_breakdown, availability, breadcrumb, image_url, feature_bullets, description, attributes, variant_asins, deal, badges, delivery_estimate, return_policy, and seller. deal is the deal the page shows: its id, its label as Amazon writes it (for example "Offre Pré-Black Friday") and its end time. badges are the other badges next to the title, for example Choix d'Amazon. The returned asin can differ from the requested one when Amazon resolves a variant. For books, brand is null and feature_bullets and attributes are usually empty. Audible audiobook ASINs open Audible's own product page instead, so they fail at once with an error that gives that page's URL.

### How do I automatically get Amazon.fr product on amazon.fr?

Ask an AI agent connected to Reduck to run reduck/amazon.fr/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/amazon.fr/get-product

### Is there a amazon.fr API to get Amazon.fr product?

You do not need one. "Get Amazon.fr product" drives the real amazon.fr pages in a browser, so it works whether or not amazon.fr offers an API for this.

### What information do I need to provide?

Required: asin. Optional: zipCode.

### What does it return?

It returns url, zip, asin, deal, brand, price, title, badges, byline, rating, seller, image_url, attributes, breadcrumb, list_price, description, availability, review_count, return_policy, variant_asins, requested_asin, feature_bullets, rating_breakdown, delivery_estimate.

### Do I need to be logged in to amazon.fr?

No. It only uses pages of amazon.fr that are reachable without signing in.

### Does it change anything on amazon.fr, or only read data?

It only reads. It looks things up on amazon.fr and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/amazon.fr/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/amazon.fr/get-product

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/amazon.fr/get-product
