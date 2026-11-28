# Add an Eight Sleep offer to the cart

Automatically add an Eight Sleep offer to the cart on eightsleep.com. Add one Eight Sleep US offer (a size, zone or pack option of a product) to the guest cart of this browser, in the quantity given, and return the cart after the add with the product id, offer id and name of the line added. Get offer ids from eightsleep.com/get_product. An offer id that the store does not sell, or a quantity below 1, is refused before the cart changes. The script does not add the items the site asks for with some products, for example the Autopilot plan with a Pod, and it does not go to checkout.

- Site: eightsleep.com
- Address: `reduck/eightsleep.com/add_to_cart`
- Updated: 2026-11-27 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/eightsleep.com/add_to_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/eightsleep.com/add_to_cart
```

## Input

- `offerId` (string, required): The offer id from eightsleep.com/get_product, e.g. variant_01JHRFW1WQ44KERHQRZWE5Y4A4.
- `quantity` (integer, optional): How many to add. 1 or more.

## Output

- `added` (boolean, required)
- `count` (integer, required)
- `lines` (array, required)
- `total` (number, required): Cart total before tax, in US dollars.
- `offerId` (string, required)
- `name` (string | null, optional)
- `productId` (string | null, optional)

## FAQ

### What does "Add an Eight Sleep offer to the cart" do?

Add one Eight Sleep US offer (a size, zone or pack option of a product) to the guest cart of this browser, in the quantity given, and return the cart after the add with the product id, offer id and name of the line added. Get offer ids from eightsleep.com/get_product. An offer id that the store does not sell, or a quantity below 1, is refused before the cart changes. The script does not add the items the site asks for with some products, for example the Autopilot plan with a Pod, and it does not go to checkout.

### How do I automatically add an Eight Sleep offer to the cart on eightsleep.com?

Ask an AI agent connected to Reduck to run reduck/eightsleep.com/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/eightsleep.com/add_to_cart

### Is there a eightsleep.com API to add an Eight Sleep offer to the cart?

You do not need one. "Add an Eight Sleep offer to the cart" drives the real eightsleep.com pages in a browser, so it works whether or not eightsleep.com offers an API for this.

### What information do I need to provide?

Required: offerId. Optional: quantity.

### What does it return?

It returns name, added, count, lines, total, offerId, productId.

### Do I need to be logged in to eightsleep.com?

No. It only uses pages of eightsleep.com that are reachable without signing in.

### Does it change anything on eightsleep.com, or only read data?

It makes changes on eightsleep.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/eightsleep.com/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/eightsleep.com/add_to_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/eightsleep.com/add_to_cart
