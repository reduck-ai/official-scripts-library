# Add to Alibaba.com cart

Automatically add to Alibaba.com cart on alibaba.com. Add a product to this browser's Alibaba.com cart, by product id and variant id, with a quantity of at least the product's minimum order quantity (the minimum order quantity when none is given), as the product page's add-to-cart button does, with the shipping method the page picks. Returns the product's cart line after the add (line id, variant, quantity, unit price, line total) and the cart totals. A product with one variant needs no variant id; for a product with more, Get Alibaba.com product lists the variant ids. Adding a variant that is already in the cart adds to its quantity. A product that the supplier sells only through a quote request, an unknown variant or a quantity under the minimum fails with an error that says so. The cart works without sign-in. List Alibaba.com cart items reads the cart; Remove from Alibaba.com cart takes the product out.

- Site: alibaba.com
- Address: `reduck/alibaba.com/add_to_cart`
- Updated: 2026-11-25 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/alibaba.com/add_to_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/alibaba.com/add_to_cart
```

## Input

- `product_id` (string, required): Alibaba.com product id, as Search Alibaba.com products gives it, or a product page link (www.alibaba.com/product-detail/..._<id>.html).
- `quantity` (integer, optional): Number of units to add, 1 to 10. It must be at least the product's minimum order quantity.
- `variant_id` (string, optional): Variant id from the variants of Get Alibaba.com product. Needed when the product has more than one variant.

## Output

- `name` (string | null, required)
- `added` (integer, required): Units added by this run.
- `count` (integer, required): Number of items in the cart after the add.
- `lines` (array, required): Every line of the cart after the add, one per product variant.
- `total` (number | null, required): Item subtotal of the cart after the add, in the display currency, shipping not included.
- `offerId` (string | null, required): Variant id that was added.
- `productId` (string, required)

## FAQ

### What does "Add to Alibaba.com cart" do?

Add a product to this browser's Alibaba.com cart, by product id and variant id, with a quantity of at least the product's minimum order quantity (the minimum order quantity when none is given), as the product page's add-to-cart button does, with the shipping method the page picks. Returns the product's cart line after the add (line id, variant, quantity, unit price, line total) and the cart totals. A product with one variant needs no variant id; for a product with more, Get Alibaba.com product lists the variant ids. Adding a variant that is already in the cart adds to its quantity. A product that the supplier sells only through a quote request, an unknown variant or a quantity under the minimum fails with an error that says so. The cart works without sign-in. List Alibaba.com cart items reads the cart; Remove from Alibaba.com cart takes the product out.

### How do I automatically add to Alibaba.com cart on alibaba.com?

Ask an AI agent connected to Reduck to run reduck/alibaba.com/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/alibaba.com/add_to_cart

### Is there a alibaba.com API to add to Alibaba.com cart?

You do not need one. "Add to Alibaba.com cart" drives the real alibaba.com pages in a browser, so it works whether or not alibaba.com offers an API for this.

### What information do I need to provide?

Required: product_id. Optional: quantity, variant_id.

### What does it return?

It returns name, added, count, lines, total, offerId, productId.

### Do I need to be logged in to alibaba.com?

No. It only uses pages of alibaba.com that are reachable without signing in.

### Does it change anything on alibaba.com, or only read data?

It makes changes on alibaba.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/alibaba.com/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/alibaba.com/add_to_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/alibaba.com/add_to_cart
