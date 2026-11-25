# Add Decathlon product to cart

Automatically add Decathlon product to cart on decathlon.fr. Add a Decathlon.fr product to the shopping cart from its product page link, with an optional quantity, and return the cart as the site holds it afterwards: each line with its product id (the sku id of the exact size), offer id, name, seller, quantity, unit price and line price in euros, plus the item count and the total. Products come in colors and sizes: the link picks the color, and the sku_id picks the size. When the color has several sizes and no sku_id is given, it fails and lists the sizes with their sku_id (Get Decathlon product lists them too). Works as a guest, with no account: the cart lives in the browser, so lines already in it stay and are listed too. Nothing is paid or ordered. A product that cannot be bought (unavailable size, out of stock) fails with an error; a link that is not a Decathlon product page fails with an error.

- Site: decathlon.fr
- Address: `reduck/decathlon.fr/add_to_cart`
- Updated: 2026-11-24 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/decathlon.fr/add_to_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/decathlon.fr/add_to_cart
```

## Input

- `url` (string, required): Link of the product page (https://www.decathlon.fr/p/...), as returned by Search Decathlon products.
- `sku_id` (string, optional): Id of the exact size to add, from the variants of Get Decathlon product. Needed when the color has several sizes; leave out when it has one.
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

### What does "Add Decathlon product to cart" do?

Add a Decathlon.fr product to the shopping cart from its product page link, with an optional quantity, and return the cart as the site holds it afterwards: each line with its product id (the sku id of the exact size), offer id, name, seller, quantity, unit price and line price in euros, plus the item count and the total. Products come in colors and sizes: the link picks the color, and the sku_id picks the size. When the color has several sizes and no sku_id is given, it fails and lists the sizes with their sku_id (Get Decathlon product lists them too). Works as a guest, with no account: the cart lives in the browser, so lines already in it stay and are listed too. Nothing is paid or ordered. A product that cannot be bought (unavailable size, out of stock) fails with an error; a link that is not a Decathlon product page fails with an error.

### How do I automatically add Decathlon product to cart on decathlon.fr?

Ask an AI agent connected to Reduck to run reduck/decathlon.fr/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/decathlon.fr/add_to_cart

### Is there a decathlon.fr API to add Decathlon product to cart?

You do not need one. "Add Decathlon product to cart" drives the real decathlon.fr pages in a browser, so it works whether or not decathlon.fr offers an API for this.

### What information do I need to provide?

Required: url. Optional: sku_id, quantity.

### What does it return?

It returns name, added, count, lines, total, offerId, productId.

### Do I need to be logged in to decathlon.fr?

No. It only uses pages of decathlon.fr that are reachable without signing in.

### Does it change anything on decathlon.fr, or only read data?

It makes changes on decathlon.fr, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/decathlon.fr/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/decathlon.fr/add_to_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/decathlon.fr/add_to_cart
