# Get Coolblue product

Automatically get Coolblue product on coolblue.nl. Get one product of Coolblue Netherlands (coolblue.nl) by its product number or product link. Returns the title, brand, price and the reference price before the reduction in euros, availability, the review score out of 10 as Coolblue gives it, the review count, the count of reviews for each number of stars and the score for each aspect, the images, the description, pros and cons, highlights, what is in the box, the specifications in their groups, the manufacturer code, the category path, the price of the second-chance (refurbished) offer, Coolblue's choice and the manual link. Texts are in Dutch. An unknown product number fails with an error that says so.

- Site: coolblue.nl
- Address: `reduck/coolblue.nl/get-product`
- Updated: 2026-11-24 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/coolblue.nl/get-product`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/coolblue.nl/get-product
```

## Input

- `product` (string, required): Coolblue product number (the product_id of Search Coolblue products) or a product link, for example https://www.coolblue.nl/product/920296/bluebuilt-nexum-silent-click-draadloze-muis.html.

## Output

- `url` (string | null, required)
- `title` (string | null, required)
- `requested` (string, required): The product number or link as the caller gave it.
- `product_id` (string, required)
- `cons` (array, optional)
- `pros` (array, optional)
- `brand` (string | null, optional)
- `price` (number | null, optional): Price in euros, VAT included.
- `images` (array, optional)
- `rating` (number | null, optional): Average review score out of 10, as Coolblue gives it. Null when the product has no review.
- `currency` (string | null, optional)
- `breadcrumb` (array, optional): Category path, from the top category to the product.
- `highlights` (array, optional)
- `list_price` (number | null, optional): Reference price in euros that the site shows struck through, null when none is shown.
- `manual_url` (string | null, optional)
- `description` (string | null, optional)
- `availability` (string | null, optional): Availability as Coolblue codes it, for example OnStock or TemporaryOutOfStock.
- `product_type` (string | null, optional): The product's category, in Dutch.
- `review_count` (integer | null, optional)
- `aspect_ratings` (array, optional): Average score out of 10 for each aspect the reviewers rate, in Dutch.
- `specifications` (array, optional): The specifications as the site groups them, names and values in Dutch.
- `included_in_box` (array, optional)
- `list_price_type` (string | null, optional): What list_price is, as Coolblue names it, for example MSRP (the manufacturer's recommended price).
- `coolblues_choice` (string | null, optional): What Coolblue chose this product for, in Dutch. Null when it is not a choice.
- `manufacturer_code` (string | null, optional)
- `rating_distribution` (array, optional): Number of reviews for each number of stars (1 to 5).
- `second_chance_price` (number | null, optional): Price in euros of Coolblue's second-chance (refurbished or returned) offer of this product, null when there is none.
- `expected_release_date` (string | null, optional)

## FAQ

### What does "Get Coolblue product" do?

Get one product of Coolblue Netherlands (coolblue.nl) by its product number or product link. Returns the title, brand, price and the reference price before the reduction in euros, availability, the review score out of 10 as Coolblue gives it, the review count, the count of reviews for each number of stars and the score for each aspect, the images, the description, pros and cons, highlights, what is in the box, the specifications in their groups, the manufacturer code, the category path, the price of the second-chance (refurbished) offer, Coolblue's choice and the manual link. Texts are in Dutch. An unknown product number fails with an error that says so.

### How do I automatically get Coolblue product on coolblue.nl?

Ask an AI agent connected to Reduck to run reduck/coolblue.nl/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/coolblue.nl/get-product

### Is there a coolblue.nl API to get Coolblue product?

You do not need one. "Get Coolblue product" drives the real coolblue.nl pages in a browser, so it works whether or not coolblue.nl offers an API for this.

### What information do I need to provide?

Required: product.

### What does it return?

It returns url, cons, pros, brand, price, title, images, rating, currency, requested, breadcrumb, highlights, list_price, manual_url, product_id, description, availability, product_type, review_count, aspect_ratings, specifications, included_in_box, list_price_type, coolblues_choice, manufacturer_code, rating_distribution, second_chance_price, expected_release_date.

### Do I need to be logged in to coolblue.nl?

No. It only uses pages of coolblue.nl that are reachable without signing in.

### Does it change anything on coolblue.nl, or only read data?

It only reads. It looks things up on coolblue.nl and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/coolblue.nl/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/coolblue.nl/get-product

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/coolblue.nl/get-product
