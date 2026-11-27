# Add John Lewis product to basket

Automatically add John Lewis product to basket on johnlewis.com. Add a product of the John Lewis UK store (johnlewis.com) to the basket of this browser, by its product number or link, with a quantity from 1 to 10, and return the whole basket afterwards: each line with its line id, product id (the sku id), offer id (always null), name with the brand, seller, quantity, unit price and line price, plus the item count, the basket total and the currency (GBP). A product with several colours or sizes needs the sku id of one of them (sku_id of Get John Lewis product). Works as a guest, with no account: lines already in the basket stay and are listed too. Nothing is paid or ordered. A variant that cannot be ordered, an unknown product number or sku id, and a link that is not a John Lewis product page fail with an error that says so. On a cloud browser, John Lewis accepts the add only from a UK address (country GB).

- Site: johnlewis.com
- Address: `reduck/johnlewis.com/add_to_cart`
- Updated: 2026-11-26 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/johnlewis.com/add_to_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/johnlewis.com/add_to_cart
```

## Input

- `product` (string, required): John Lewis product number (product_id of Search John Lewis products) or product link (https://www.johnlewis.com/<name>/p<number>).
- `sku_id` (string, optional): Sku id of the colour or size to add (sku_id of Get John Lewis product). Needed when the product has more than one variant.
- `quantity` (integer, optional): Number of units to add, 1 to 10.

## Output

- `name` (string | null, required)
- `added` (integer, required): Units added by this call.
- `count` (integer, required): Number of units in the basket after the add, all lines together.
- `lines` (array, required)
- `total` (number | null, required): Basket subtotal before delivery, in pounds sterling.
- `offerId` (string | null, required): Always null: John Lewis has no offer id.
- `currency` (string, required): GBP
- `productId` (string, required): Sku id of the variant added, as in the basket lines.

## FAQ

### What does "Add John Lewis product to basket" do?

Add a product of the John Lewis UK store (johnlewis.com) to the basket of this browser, by its product number or link, with a quantity from 1 to 10, and return the whole basket afterwards: each line with its line id, product id (the sku id), offer id (always null), name with the brand, seller, quantity, unit price and line price, plus the item count, the basket total and the currency (GBP). A product with several colours or sizes needs the sku id of one of them (sku_id of Get John Lewis product). Works as a guest, with no account: lines already in the basket stay and are listed too. Nothing is paid or ordered. A variant that cannot be ordered, an unknown product number or sku id, and a link that is not a John Lewis product page fail with an error that says so. On a cloud browser, John Lewis accepts the add only from a UK address (country GB).

### How do I automatically add John Lewis product to basket on johnlewis.com?

Ask an AI agent connected to Reduck to run reduck/johnlewis.com/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/johnlewis.com/add_to_cart

### Is there a johnlewis.com API to add John Lewis product to basket?

You do not need one. "Add John Lewis product to basket" drives the real johnlewis.com pages in a browser, so it works whether or not johnlewis.com offers an API for this.

### What information do I need to provide?

Required: product. Optional: sku_id, quantity.

### What does it return?

It returns name, added, count, lines, total, offerId, currency, productId.

### Do I need to be logged in to johnlewis.com?

No. It only uses pages of johnlewis.com that are reachable without signing in.

### Does it change anything on johnlewis.com, or only read data?

It makes changes on johnlewis.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/johnlewis.com/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/johnlewis.com/add_to_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/johnlewis.com/add_to_cart
