# Add to Gifi cart

Automatically add to Gifi cart on gifi.fr. Add a Gifi.fr product to the guest cart of this browser, from its product id or product page link, with a quantity from 1 to 10, and return the cart afterwards: the unit count, the item subtotal in euros and each line with its product id, name, seller, quantity, unit price and line price. A product id Gifi does not know fails with an error. Nothing is paid or ordered.

- Site: gifi.fr
- Address: `reduck/gifi.fr/add_to_cart`
- Updated: 2026-11-25 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/gifi.fr/add_to_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/gifi.fr/add_to_cart
```

## Input

- `product` (string, required): Gifi product id (e.g. 000000000000577264 or 577264) or product page link, as Search Gifi products returns them.
- `quantity` (integer, optional): Units to add, 1 to 10.

## Output

- `name` (string | null, required)
- `added` (integer, required): Units this run added.
- `count` (integer, required): Units in the cart.
- `lines` (array, required)
- `total` (number | null, required): Item subtotal in euros, without delivery.
- `offerId` (string | null, required)
- `productId` (string, required)

## FAQ

### What does "Add to Gifi cart" do?

Add a Gifi.fr product to the guest cart of this browser, from its product id or product page link, with a quantity from 1 to 10, and return the cart afterwards: the unit count, the item subtotal in euros and each line with its product id, name, seller, quantity, unit price and line price. A product id Gifi does not know fails with an error. Nothing is paid or ordered.

### How do I automatically add to Gifi cart on gifi.fr?

Ask an AI agent connected to Reduck to run reduck/gifi.fr/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/gifi.fr/add_to_cart

### Is there a gifi.fr API to add to Gifi cart?

You do not need one. "Add to Gifi cart" drives the real gifi.fr pages in a browser, so it works whether or not gifi.fr offers an API for this.

### What information do I need to provide?

Required: product. Optional: quantity.

### What does it return?

It returns name, added, count, lines, total, offerId, productId.

### Do I need to be logged in to gifi.fr?

No. It only uses pages of gifi.fr that are reachable without signing in.

### Does it change anything on gifi.fr, or only read data?

It makes changes on gifi.fr, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/gifi.fr/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/gifi.fr/add_to_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/gifi.fr/add_to_cart
