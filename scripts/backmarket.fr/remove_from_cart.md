# Remove Back Market France product from cart

Automatically remove Back Market France product from cart on backmarket.fr. Remove a product from the backmarket.fr cart of this browser by its product id, whatever its quantity, and return what is left in the cart: each line with its product id, offer id, name, seller, condition grade, quantity, unit price and line price in euros, plus the item count and total. A product that is not in the cart is reported with removed false and the cart unchanged, not as a failure. When the same product is in the cart from several sellers or in several grades, pass the offer id to pick the line.

- Site: backmarket.fr
- Address: `reduck/backmarket.fr/remove_from_cart`
- Updated: 2026-11-24 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/backmarket.fr/remove_from_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/backmarket.fr/remove_from_cart
```

## Input

- `productId` (string, required): Product id of the cart line, as List Back Market France cart items returns it.
- `offerId` (string, optional): Offer id, to pick one line when the product is in the cart from several sellers or grades.

## Output

- `count` (integer, required)
- `lines` (array, required)
- `removed` (boolean, required)
- `total` (number | null, optional)

## FAQ

### What does "Remove Back Market France product from cart" do?

Remove a product from the backmarket.fr cart of this browser by its product id, whatever its quantity, and return what is left in the cart: each line with its product id, offer id, name, seller, condition grade, quantity, unit price and line price in euros, plus the item count and total. A product that is not in the cart is reported with removed false and the cart unchanged, not as a failure. When the same product is in the cart from several sellers or in several grades, pass the offer id to pick the line.

### How do I automatically remove Back Market France product from cart on backmarket.fr?

Ask an AI agent connected to Reduck to run reduck/backmarket.fr/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/backmarket.fr/remove_from_cart

### Is there a backmarket.fr API to remove Back Market France product from cart?

You do not need one. "Remove Back Market France product from cart" drives the real backmarket.fr pages in a browser, so it works whether or not backmarket.fr offers an API for this.

### What information do I need to provide?

Required: productId. Optional: offerId.

### What does it return?

It returns count, lines, total, removed.

### Do I need to be logged in to backmarket.fr?

No. It only uses pages of backmarket.fr that are reachable without signing in.

### Does it change anything on backmarket.fr, or only read data?

It makes changes on backmarket.fr, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/backmarket.fr/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/backmarket.fr/remove_from_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/backmarket.fr/remove_from_cart
