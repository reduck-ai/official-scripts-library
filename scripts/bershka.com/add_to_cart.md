# Add Bershka product to cart

Automatically add Bershka product to cart on bershka.com. Add one size of a Bershka France (bershka.com/fr) product to the cart of this browser, with a quantity from 1 to 10. Give the product id or link and the offerId of the size and length from Get Bershka product. Returns the cart after the add (each line, the number of units and the total in euros) with the product id, offerId, name and number of units added. A size that is not in stock, or an offerId that is not on the product, gives an error with the sizes of the product. Works without sign-in: the cart stays with the browser, and lines already in it stay. Bershka can refuse the add from a browser outside France: then the run fails and says so. Nothing is paid or ordered.

- Site: bershka.com
- Address: `reduck/bershka.com/add_to_cart`
- Updated: 2026-11-27 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/bershka.com/add_to_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/bershka.com/add_to_cart
```

## Input

- `offerId` (string, required): Id of the size to add (offerId of a size in Get Bershka product).
- `product` (string, required): Product id or product page link, from Search Bershka products or Get Bershka product.
- `quantity` (integer, optional): Number of units to add, 1 to 10.

## Output

- `name` (string | null, required)
- `added` (integer, required): Number of units added.
- `count` (integer, required): Number of units in the cart.
- `lines` (array, required)
- `total` (number | null, required): Total of the cart, in euros.
- `offerId` (string, required)
- `currency` (string, required): Currency of the amounts, as an ISO code (euro).
- `productId` (string, required)

## FAQ

### What does "Add Bershka product to cart" do?

Add one size of a Bershka France (bershka.com/fr) product to the cart of this browser, with a quantity from 1 to 10. Give the product id or link and the offerId of the size and length from Get Bershka product. Returns the cart after the add (each line, the number of units and the total in euros) with the product id, offerId, name and number of units added. A size that is not in stock, or an offerId that is not on the product, gives an error with the sizes of the product. Works without sign-in: the cart stays with the browser, and lines already in it stay. Bershka can refuse the add from a browser outside France: then the run fails and says so. Nothing is paid or ordered.

### How do I automatically add Bershka product to cart on bershka.com?

Ask an AI agent connected to Reduck to run reduck/bershka.com/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/bershka.com/add_to_cart

### Is there a bershka.com API to add Bershka product to cart?

You do not need one. "Add Bershka product to cart" drives the real bershka.com pages in a browser, so it works whether or not bershka.com offers an API for this.

### What information do I need to provide?

Required: product, offerId. Optional: quantity.

### What does it return?

It returns name, added, count, lines, total, offerId, currency, productId.

### Do I need to be logged in to bershka.com?

No. It only uses pages of bershka.com that are reachable without signing in.

### Does it change anything on bershka.com, or only read data?

It makes changes on bershka.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/bershka.com/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/bershka.com/add_to_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/bershka.com/add_to_cart
