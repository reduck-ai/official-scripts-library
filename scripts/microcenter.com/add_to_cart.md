# Add a product to the Micro Center cart

Automatically add a product to the Micro Center cart on microcenter.com. Add a Micro Center (microcenter.com) product to the cart of this browser, by its link or product id, with a quantity from 1 to 10, and return the whole cart afterwards: each line with its line id, product id, offer id (always null), name, seller (always Micro Center), quantity, unit price and line price in US dollars, plus the item count and the cart total Micro Center shows (before tax, with the shipping price of shippable items). Works as a guest, with no account: lines already in the cart stay and are listed too. The product is bought from the web store 029 (shippable items) unless store_id names a store for pickup. Nothing is paid or ordered. A product the store does not sell online, an unknown product id, a link that is not a Micro Center product page and a quantity above Micro Center's limit fail with an error that says so.

- Site: microcenter.com
- Address: `reduck/microcenter.com/add_to_cart`
- Updated: 2026-11-26 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/microcenter.com/add_to_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/microcenter.com/add_to_cart
```

## Input

- `url` (string, optional): Micro Center product link (https://www.microcenter.com/product/<id>/<name>), as Search Micro Center products returns it.
- `quantity` (integer, optional): Number of units to add, 1 to 10.
- `store_id` (string, optional): Micro Center store to buy from, three digits from the site's store picker, for example 081 (Fairfax, VA) for in-store pickup. Omit for the web store 029 (shippable items).
- `product_id` (string, optional): Micro Center product id (product_id of Search Micro Center products). Used when no url is given.

## Output

- `name` (string | null, required)
- `added` (integer, required): Units added by this call.
- `count` (integer, required): Number of units in the cart after the add, all lines together.
- `lines` (array, required)
- `total` (number | null, required): Cart total in US dollars as Micro Center shows it, before tax, with the shipping price of shippable items.
- `offerId` (string | null, required): Always null: Micro Center sells its products itself.
- `productId` (string, required): Micro Center product id of the product added.

## FAQ

### What does "Add a product to the Micro Center cart" do?

Add a Micro Center (microcenter.com) product to the cart of this browser, by its link or product id, with a quantity from 1 to 10, and return the whole cart afterwards: each line with its line id, product id, offer id (always null), name, seller (always Micro Center), quantity, unit price and line price in US dollars, plus the item count and the cart total Micro Center shows (before tax, with the shipping price of shippable items). Works as a guest, with no account: lines already in the cart stay and are listed too. The product is bought from the web store 029 (shippable items) unless store_id names a store for pickup. Nothing is paid or ordered. A product the store does not sell online, an unknown product id, a link that is not a Micro Center product page and a quantity above Micro Center's limit fail with an error that says so.

### How do I automatically add a product to the Micro Center cart on microcenter.com?

Ask an AI agent connected to Reduck to run reduck/microcenter.com/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/microcenter.com/add_to_cart

### Is there a microcenter.com API to add a product to the Micro Center cart?

You do not need one. "Add a product to the Micro Center cart" drives the real microcenter.com pages in a browser, so it works whether or not microcenter.com offers an API for this.

### What information do I need to provide?

Optional: url, quantity, store_id, product_id.

### What does it return?

It returns name, added, count, lines, total, offerId, productId.

### Do I need to be logged in to microcenter.com?

No. It only uses pages of microcenter.com that are reachable without signing in.

### Does it change anything on microcenter.com, or only read data?

It makes changes on microcenter.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/microcenter.com/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/microcenter.com/add_to_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/microcenter.com/add_to_cart
