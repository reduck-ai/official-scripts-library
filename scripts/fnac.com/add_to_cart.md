# Add a Fnac product to the cart

Automatically add a Fnac product to the cart on fnac.com. Add a Fnac.com product to the shopping cart from its id (a<number> or mp<number>, as Search Fnac products returns) or its product page link, with a quantity from 1 to 10, and return the cart as the site holds it afterwards: each line with its product id, offer id, name, seller, quantity, unit price and line price in euros, plus the item count and total. Works as a guest, with no account: the cart lives in the browser, so lines already in it stay and are listed too. The product is added from the offer Fnac shows first; to buy from another seller, pass the offer id from Get Fnac product's offers, or a link that carries it. The seller of each line is named in the cart. Nothing is paid or ordered. A product that has no add button (unavailable) fails with an error, and so does a link that is not a Fnac product page.

- Site: fnac.com
- Address: `reduck/fnac.com/add_to_cart`
- Updated: 2026-11-25 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/fnac.com/add_to_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/fnac.com/add_to_cart
```

## Input

- `product` (string, required): Fnac product id as Search Fnac products returns it (a<number> or mp<number>), or a www.fnac.com product page link. A link ending with ?oref=<offer id> selects that seller's offer.
- `offer_id` (string | null, optional): Offer id from the offers of Get Fnac product, to buy from that seller instead of the offer Fnac shows first. Leave out for the default offer.
- `quantity` (integer, optional): Units to add, 1 to 10. Added to what the cart already holds for the same offer.

## Output

- `name` (string | null, required)
- `added` (boolean, required)
- `count` (integer, required): Number of items in the cart, quantities summed.
- `lines` (array, required)
- `total` (number | null, required): Cart total in euros as the site states it.
- `productId` (string, required): Fnac numeric product id of the line that was added.
- `offerId` (string | null, optional)

## FAQ

### What does "Add a Fnac product to the cart" do?

Add a Fnac.com product to the shopping cart from its id (a<number> or mp<number>, as Search Fnac products returns) or its product page link, with a quantity from 1 to 10, and return the cart as the site holds it afterwards: each line with its product id, offer id, name, seller, quantity, unit price and line price in euros, plus the item count and total. Works as a guest, with no account: the cart lives in the browser, so lines already in it stay and are listed too. The product is added from the offer Fnac shows first; to buy from another seller, pass the offer id from Get Fnac product's offers, or a link that carries it. The seller of each line is named in the cart. Nothing is paid or ordered. A product that has no add button (unavailable) fails with an error, and so does a link that is not a Fnac product page.

### How do I automatically add a Fnac product to the cart on fnac.com?

Ask an AI agent connected to Reduck to run reduck/fnac.com/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/fnac.com/add_to_cart

### Is there a fnac.com API to add a Fnac product to the cart?

You do not need one. "Add a Fnac product to the cart" drives the real fnac.com pages in a browser, so it works whether or not fnac.com offers an API for this.

### What information do I need to provide?

Required: product. Optional: offer_id, quantity.

### What does it return?

It returns name, added, count, lines, total, offerId, productId.

### Do I need to be logged in to fnac.com?

No. It only uses pages of fnac.com that are reachable without signing in.

### Does it change anything on fnac.com, or only read data?

It makes changes on fnac.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/fnac.com/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/fnac.com/add_to_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/fnac.com/add_to_cart
