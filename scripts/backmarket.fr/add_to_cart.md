# Add Back Market France product to cart

Automatically add Back Market France product to cart on backmarket.fr. Add a backmarket.fr product to the shopping cart from its product page link, with an optional quantity, and return the cart as the site holds it afterwards: each line with its product id, offer id, name, seller, condition grade, quantity, unit price and line price in euros, plus the item count and total. The grade in the link (l parameter) decides which offer and which seller are added. Works as a guest, with no account: the cart lives in the browser, so lines already in it stay and are listed too. Nothing is paid or ordered. A product that is out of stock, or a link that is not a Back Market product page, fails with an error.

- Site: backmarket.fr
- Address: `reduck/backmarket.fr/add_to_cart`
- Updated: 2026-11-24 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/backmarket.fr/add_to_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/backmarket.fr/add_to_cart
```

## Input

- `link` (string, required): Product page link on www.backmarket.fr, from Search Back Market France products (with the grade in l=).
- `quantity` (integer, optional): How many units to add, 1 to 10.

## Output

- `added` (boolean, required)
- `count` (integer, required)
- `lines` (array, required)
- `productId` (string, required)
- `name` (string | null, optional)
- `total` (number | null, optional)
- `offerId` (string | null, optional)

## FAQ

### What does "Add Back Market France product to cart" do?

Add a backmarket.fr product to the shopping cart from its product page link, with an optional quantity, and return the cart as the site holds it afterwards: each line with its product id, offer id, name, seller, condition grade, quantity, unit price and line price in euros, plus the item count and total. The grade in the link (l parameter) decides which offer and which seller are added. Works as a guest, with no account: the cart lives in the browser, so lines already in it stay and are listed too. Nothing is paid or ordered. A product that is out of stock, or a link that is not a Back Market product page, fails with an error.

### How do I automatically add Back Market France product to cart on backmarket.fr?

Ask an AI agent connected to Reduck to run reduck/backmarket.fr/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/backmarket.fr/add_to_cart

### Is there a backmarket.fr API to add Back Market France product to cart?

You do not need one. "Add Back Market France product to cart" drives the real backmarket.fr pages in a browser, so it works whether or not backmarket.fr offers an API for this.

### What information do I need to provide?

Required: link. Optional: quantity.

### What does it return?

It returns name, added, count, lines, total, offerId, productId.

### Do I need to be logged in to backmarket.fr?

No. It only uses pages of backmarket.fr that are reachable without signing in.

### Does it change anything on backmarket.fr, or only read data?

It makes changes on backmarket.fr, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/backmarket.fr/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/backmarket.fr/add_to_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/backmarket.fr/add_to_cart
