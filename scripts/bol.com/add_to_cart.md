# Add bol.com product to cart

Automatically add bol.com product to cart on bol.com. Add a bol.com product (Netherlands, Dutch site) to the shopping cart from its product id or page link, with an optional quantity, and return the cart as the site answers after the add: each line with its product id, offer id, name, seller, quantity, unit price and line price in euros, the item count and the total of the articles in euros (delivery not included). Works as a guest, with no account: the cart lives in the browser, so lines already in it stay and are listed too. Nothing is paid or ordered. A product with no offer on sale, or with no add button on its page, fails with an error; an id or link that is not a bol.com product fails with an error.

- Site: bol.com
- Address: `reduck/bol.com/add_to_cart`
- Updated: 2026-11-24 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/bol.com/add_to_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/bol.com/add_to_cart
```

## Input

- `product` (string, required): A bol.com product id as returned by Search bol.com products (for example 9300000000353594), or the link of a bol.com product page.
- `quantity` (integer, optional): How many units to add to the cart.

## Output

- `name` (string | null, required)
- `added` (integer, required): Units this run added to the cart.
- `count` (integer, required): Units in the cart after the add.
- `lines` (array, required)
- `total` (number | null, required): Total of the articles in the cart in euros, delivery not included.
- `offerId` (string, required)
- `productId` (string, required)

## FAQ

### What does "Add bol.com product to cart" do?

Add a bol.com product (Netherlands, Dutch site) to the shopping cart from its product id or page link, with an optional quantity, and return the cart as the site answers after the add: each line with its product id, offer id, name, seller, quantity, unit price and line price in euros, the item count and the total of the articles in euros (delivery not included). Works as a guest, with no account: the cart lives in the browser, so lines already in it stay and are listed too. Nothing is paid or ordered. A product with no offer on sale, or with no add button on its page, fails with an error; an id or link that is not a bol.com product fails with an error.

### How do I automatically add bol.com product to cart on bol.com?

Ask an AI agent connected to Reduck to run reduck/bol.com/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/bol.com/add_to_cart

### Is there a bol.com API to add bol.com product to cart?

You do not need one. "Add bol.com product to cart" drives the real bol.com pages in a browser, so it works whether or not bol.com offers an API for this.

### What information do I need to provide?

Required: product. Optional: quantity.

### What does it return?

It returns name, added, count, lines, total, offerId, productId.

### Do I need to be logged in to bol.com?

No. It only uses pages of bol.com that are reachable without signing in.

### Does it change anything on bol.com, or only read data?

It makes changes on bol.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/bol.com/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/bol.com/add_to_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/bol.com/add_to_cart
