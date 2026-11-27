# Add to Bed Bath & Beyond cart

Automatically add to Bed Bath & Beyond cart on bedbathandbeyond.com. Add a Bed Bath & Beyond product to the cart of this browser, from its id or page link, with a quantity from 1 to 10. A product sold in several options (color, size) needs optionId, from get-product. Gives the cart after the add. An unknown product, an unknown option, a missing option, a product out of stock, or a quantity above the site's limit gives an error that says so, and nothing is added.

- Site: bedbathandbeyond.com
- Address: `reduck/bedbathandbeyond.com/add_to_cart`
- Updated: 2026-11-26 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/bedbathandbeyond.com/add_to_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/bedbathandbeyond.com/add_to_cart
```

## Input

- `product` (string, required): The product id (from search-products) or the link of its page on bedbathandbeyond.com.
- `optionId` (string, optional): The id of the option to add (a variant id from get-product). Needed when the product has more than one option.
- `quantity` (integer, optional): How many to add.

## Output

- `name` (string | null, required)
- `added` (boolean, required)
- `count` (integer, required): The number of items in the cart after the add, all quantities added.
- `lines` (array, required)
- `total` (number | null, required): The cart total in US dollars.
- `offerId` (string | null, required): The option id that was added.
- `productId` (string | null, required)

## FAQ

### What does "Add to Bed Bath & Beyond cart" do?

Add a Bed Bath & Beyond product to the cart of this browser, from its id or page link, with a quantity from 1 to 10. A product sold in several options (color, size) needs optionId, from get-product. Gives the cart after the add. An unknown product, an unknown option, a missing option, a product out of stock, or a quantity above the site's limit gives an error that says so, and nothing is added.

### How do I automatically add to Bed Bath & Beyond cart on bedbathandbeyond.com?

Ask an AI agent connected to Reduck to run reduck/bedbathandbeyond.com/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/bedbathandbeyond.com/add_to_cart

### Is there a bedbathandbeyond.com API to add to Bed Bath & Beyond cart?

You do not need one. "Add to Bed Bath & Beyond cart" drives the real bedbathandbeyond.com pages in a browser, so it works whether or not bedbathandbeyond.com offers an API for this.

### What information do I need to provide?

Required: product. Optional: optionId, quantity.

### What does it return?

It returns name, added, count, lines, total, offerId, productId.

### Do I need to be logged in to bedbathandbeyond.com?

No. It only uses pages of bedbathandbeyond.com that are reachable without signing in.

### Does it change anything on bedbathandbeyond.com, or only read data?

It makes changes on bedbathandbeyond.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/bedbathandbeyond.com/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/bedbathandbeyond.com/add_to_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/bedbathandbeyond.com/add_to_cart
