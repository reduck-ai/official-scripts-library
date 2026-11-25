# Add to IKEA France cart

Automatically add to IKEA France cart on ikea.com. Add an IKEA France (ikea.com/fr/fr) product to the shopping cart from its article number or product link, with a quantity from 1 to 10, and return the cart as the site holds it afterwards: each line with its article number, name, quantity, unit price and line price in euros, plus the item count and total. Works as a guest, with no account: the cart lives in the browser, so lines already in it stay and are listed too. Nothing is paid or ordered. A product that cannot be bought online (store only, coming soon, withdrawn) fails with an error; a link that is not an IKEA France product page fails with an error. The product page opens the exact article: pass the article number of the size or color you want (see Get IKEA France product, variations).

- Site: ikea.com
- Address: `reduck/ikea.com/add_to_cart`
- Updated: 2026-11-24 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/ikea.com/add_to_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/ikea.com/add_to_cart
```

## Input

- `product` (string, required): The 8-digit article number (for example 20608733) or the product page link on ikea.com/fr/fr.
- `quantity` (integer, optional): How many to add, 1 to 10.

## Output

- `added` (integer, required)
- `count` (integer, required)
- `lines` (array, required)
- `productId` (string, required)
- `name` (string | null, optional)
- `total` (number | null, optional)
- `offerId` (string | null, optional)

## FAQ

### What does "Add to IKEA France cart" do?

Add an IKEA France (ikea.com/fr/fr) product to the shopping cart from its article number or product link, with a quantity from 1 to 10, and return the cart as the site holds it afterwards: each line with its article number, name, quantity, unit price and line price in euros, plus the item count and total. Works as a guest, with no account: the cart lives in the browser, so lines already in it stay and are listed too. Nothing is paid or ordered. A product that cannot be bought online (store only, coming soon, withdrawn) fails with an error; a link that is not an IKEA France product page fails with an error. The product page opens the exact article: pass the article number of the size or color you want (see Get IKEA France product, variations).

### How do I automatically add to IKEA France cart on ikea.com?

Ask an AI agent connected to Reduck to run reduck/ikea.com/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/ikea.com/add_to_cart

### Is there a ikea.com API to add to IKEA France cart?

You do not need one. "Add to IKEA France cart" drives the real ikea.com pages in a browser, so it works whether or not ikea.com offers an API for this.

### What information do I need to provide?

Required: product. Optional: quantity.

### What does it return?

It returns name, added, count, lines, total, offerId, productId.

### Do I need to be logged in to ikea.com?

No. It only uses pages of ikea.com that are reachable without signing in.

### Does it change anything on ikea.com, or only read data?

It makes changes on ikea.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/ikea.com/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/ikea.com/add_to_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/ikea.com/add_to_cart
