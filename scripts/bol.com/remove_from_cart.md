# Remove bol.com product from cart

Automatically remove bol.com product from cart on bol.com. Remove a product from the bol.com cart (Netherlands, Dutch site) of this browser by its product id or page link, whatever its quantity, and return what is left in the cart: each line with its product id, offer id, name, seller, quantity, unit price and line price in euros, the item count and the total of the articles in euros (delivery not included). A product that is not in the cart is reported with removed false and the cart unchanged, not as a failure. An id or link that is not a bol.com product fails with an error.

- Site: bol.com
- Address: `reduck/bol.com/remove_from_cart`
- Updated: 2026-11-24 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/bol.com/remove_from_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/bol.com/remove_from_cart
```

## Input

- `product` (string, required): A bol.com product id as returned by List bol.com cart items (for example 9300000000353594), or the link of a bol.com product page.

## Output

- `count` (integer, required): Units left in the cart.
- `lines` (array, required)
- `total` (number | null, required): Total of the articles left in euros, delivery not included.
- `removed` (boolean, required): False when the product was not in the cart.
- `productId` (string, required)

## FAQ

### What does "Remove bol.com product from cart" do?

Remove a product from the bol.com cart (Netherlands, Dutch site) of this browser by its product id or page link, whatever its quantity, and return what is left in the cart: each line with its product id, offer id, name, seller, quantity, unit price and line price in euros, the item count and the total of the articles in euros (delivery not included). A product that is not in the cart is reported with removed false and the cart unchanged, not as a failure. An id or link that is not a bol.com product fails with an error.

### How do I automatically remove bol.com product from cart on bol.com?

Ask an AI agent connected to Reduck to run reduck/bol.com/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/bol.com/remove_from_cart

### Is there a bol.com API to remove bol.com product from cart?

You do not need one. "Remove bol.com product from cart" drives the real bol.com pages in a browser, so it works whether or not bol.com offers an API for this.

### What information do I need to provide?

Required: product.

### What does it return?

It returns count, lines, total, removed, productId.

### Do I need to be logged in to bol.com?

No. It only uses pages of bol.com that are reachable without signing in.

### Does it change anything on bol.com, or only read data?

It makes changes on bol.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/bol.com/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/bol.com/remove_from_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/bol.com/remove_from_cart
