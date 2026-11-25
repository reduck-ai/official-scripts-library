# Add H&M France product to cart

Automatically add H&M France product to cart on hm.com. Add one size of an H&M France product (hm.com/fr_fr) to the guest cart of this browser, with a quantity from 1 to 10, and return the cart as the site holds it afterwards: each line with variant id, product id, name, brand, size, color, quantity, unit price and line price in euros, plus the item count and the items subtotal. Pass the variant id (product id plus size code, from Search or Get H&M France product). Given only a product id or a link, it fails with the list of sizes and their variant ids. A size that is out of stock fails with an error. Nothing is paid or ordered.

- Site: hm.com
- Address: `reduck/hm.com/add_to_cart`
- Updated: 2026-11-24 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/hm.com/add_to_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/hm.com/add_to_cart
```

## Input

- `product` (string, required): Variant id (13 digits: product id plus size code, for example 0685816001003 for size M), as returned by Search H&M France products or Get H&M France product. A product id or a product link is refused with the list of its variants.
- `quantity` (integer, optional): Number of units to add.

## Output

- `name` (string | null, required)
- `added` (integer, required)
- `count` (integer, required)
- `lines` (array, required)
- `total` (number | null, required)
- `offerId` (string, required)
- `productId` (string, required)

## FAQ

### What does "Add H&M France product to cart" do?

Add one size of an H&M France product (hm.com/fr_fr) to the guest cart of this browser, with a quantity from 1 to 10, and return the cart as the site holds it afterwards: each line with variant id, product id, name, brand, size, color, quantity, unit price and line price in euros, plus the item count and the items subtotal. Pass the variant id (product id plus size code, from Search or Get H&M France product). Given only a product id or a link, it fails with the list of sizes and their variant ids. A size that is out of stock fails with an error. Nothing is paid or ordered.

### How do I automatically add H&M France product to cart on hm.com?

Ask an AI agent connected to Reduck to run reduck/hm.com/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/hm.com/add_to_cart

### Is there a hm.com API to add H&M France product to cart?

You do not need one. "Add H&M France product to cart" drives the real hm.com pages in a browser, so it works whether or not hm.com offers an API for this.

### What information do I need to provide?

Required: product. Optional: quantity.

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
