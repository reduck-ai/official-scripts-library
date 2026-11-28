# Add a product to the Nykaa bag

Automatically add a product to the Nykaa bag on nykaa.com. Add a product of the Nykaa India store (nykaa.com) to the bag of this browser, in the quantity you give. A product with shades or sizes needs variantId, from get-product. It returns the product id added and the bag after the change (lines, units, grand total in Indian rupees). It refuses an unknown product, a missing or wrong shade or size, a product out of stock, and a quantity below 1 or above the limit Nykaa sets for the product. It adds to the guest bag when nobody is signed in; Nykaa needs no delivery pincode for it. It never goes to checkout.

- Site: nykaa.com
- Address: `reduck/nykaa.com/add_to_cart`
- Updated: 2026-11-27 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/nykaa.com/add_to_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/nykaa.com/add_to_cart
```

## Input

- `productId` (string, required): Nykaa product id, as search-products or get-product returns it.
- `quantity` (integer, optional): Number of units to add. Nykaa sets a limit for each product, often 10.
- `variantId` (string, optional): Shade or size id from the variants of get-product. Required when the product has shades or sizes.

## Output

- `name` (string, required)
- `added` (boolean, required)
- `count` (integer, required): Number of units in the bag.
- `lines` (array, required)
- `total` (number | null, required): Grand total of the bag in Indian rupees. Null when the bag is empty.
- `offerId` (string, required)
- `currency` (string, required): INR
- `productId` (string, required): Id that was added (the shade or size id for a product with variants).

## FAQ

### What does "Add a product to the Nykaa bag" do?

Add a product of the Nykaa India store (nykaa.com) to the bag of this browser, in the quantity you give. A product with shades or sizes needs variantId, from get-product. It returns the product id added and the bag after the change (lines, units, grand total in Indian rupees). It refuses an unknown product, a missing or wrong shade or size, a product out of stock, and a quantity below 1 or above the limit Nykaa sets for the product. It adds to the guest bag when nobody is signed in; Nykaa needs no delivery pincode for it. It never goes to checkout.

### How do I automatically add a product to the Nykaa bag on nykaa.com?

Ask an AI agent connected to Reduck to run reduck/nykaa.com/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/nykaa.com/add_to_cart

### Is there a nykaa.com API to add a product to the Nykaa bag?

You do not need one. "Add a product to the Nykaa bag" drives the real nykaa.com pages in a browser, so it works whether or not nykaa.com offers an API for this.

### What information do I need to provide?

Required: productId. Optional: quantity, variantId.

### What does it return?

It returns name, added, count, lines, total, offerId, currency, productId.

### Do I need to be logged in to nykaa.com?

No. It only uses pages of nykaa.com that are reachable without signing in.

### Does it change anything on nykaa.com, or only read data?

It makes changes on nykaa.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/nykaa.com/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/nykaa.com/add_to_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/nykaa.com/add_to_cart
