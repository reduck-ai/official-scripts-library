# Add H&M France product to cart

Automatically add H&M France product to cart on hm.com. Add an H&M France product (hm.com/fr_fr) to the guest cart of this browser, with a quantity from 1 to 10, and return the cart as the site holds it afterwards: the item count, the items subtotal in euros and each line with its product id, variant id (offerId, which names the size), name, seller, quantity, unit price and line price. Pass a variant id, or a product id or link with a size label. A product with one size needs no size label. A size that is out of stock, or a link that is not a product, fails with an error. Nothing is paid or ordered.

- Site: hm.com
- Address: `reduck/hm.com/add_to_cart`
- Updated: 2026-11-25 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/hm.com/add_to_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/hm.com/add_to_cart
```

## Input

- `product` (string, required): Product id (10 digits, for example 0685816001; it includes the color), variant id (13 digits: product id plus size code, for example 0685816001003 for size M) or a link to an H&M France product page, as returned by Search H&M France products or Get H&M France product.
- `size` (string, optional): Size label as the product lists it (for example "M" or "134/140 (8-10Y)"). Needed with a product id or link when the product has several sizes; not used with a variant id.
- `quantity` (integer, optional): Number of units to add, 1 to 10.

## Output

- `name` (string | null, required)
- `added` (integer, required)
- `count` (integer, required)
- `lines` (array, required)
- `total` (number | null, required)
- `offerId` (string | null, required)
- `productId` (string, required)

## FAQ

### What does "Add H&M France product to cart" do?

Add an H&M France product (hm.com/fr_fr) to the guest cart of this browser, with a quantity from 1 to 10, and return the cart as the site holds it afterwards: the item count, the items subtotal in euros and each line with its product id, variant id (offerId, which names the size), name, seller, quantity, unit price and line price. Pass a variant id, or a product id or link with a size label. A product with one size needs no size label. A size that is out of stock, or a link that is not a product, fails with an error. Nothing is paid or ordered.

### How do I automatically add H&M France product to cart on hm.com?

Ask an AI agent connected to Reduck to run reduck/hm.com/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/hm.com/add_to_cart

### Is there a hm.com API to add H&M France product to cart?

You do not need one. "Add H&M France product to cart" drives the real hm.com pages in a browser, so it works whether or not hm.com offers an API for this.

### What information do I need to provide?

Required: product. Optional: size, quantity.

### What does it return?

It returns name, added, count, lines, total, offerId, productId.

### Do I need to be logged in to hm.com?

No. It only uses pages of hm.com that are reachable without signing in.

### Does it change anything on hm.com, or only read data?

It makes changes on hm.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/hm.com/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/hm.com/add_to_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/hm.com/add_to_cart
