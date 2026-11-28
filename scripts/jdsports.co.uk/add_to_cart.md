# Add a product to the JD Sports cart

Automatically add a product to the JD Sports cart on jdsports.co.uk. Add one size of a product of JD Sports UK (jdsports.co.uk, the United Kingdom store) to the shopping bag of this browser, from its JD Sports product id or product page link and its size (or the size sku from Get JD Sports product), with a quantity, as the product page's size and add to bag buttons do. A product with one size needs no size. Returns the product id, the size sku (offerId), name and size added, the units added, and the bag after the add: each line with its line id, product id, size sku, name, size, quantity, unit price and line price in pounds (GBP), the item count, the total with promotions applied, the subtotal and the currency. Works as a guest, with no account: lines already in the bag stay. Nothing is ordered or paid. An unknown product, a size the product does not have, a size out of stock, or an add the site refuses fails with an error that says so.

- Site: jdsports.co.uk
- Address: `reduck/jdsports.co.uk/add_to_cart`
- Updated: 2026-11-27 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/jdsports.co.uk/add_to_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/jdsports.co.uk/add_to_cart
```

## Input

- `product` (string, required): A JD Sports product id as Search JD Sports products returns it, for example 19760893, or a jdsports.co.uk product page link.
- `size` (string, optional): The size as the product page writes it, for example M or 9. Leave it out for a product with one size, or pass offerId instead.
- `offerId` (string, optional): The sku of the size, from the variants of Get JD Sports product.
- `quantity` (integer, optional): How many units to add.

## Output

- `name` (string | null, required)
- `size` (string | null, required)
- `added` (integer, required): Units this run added.
- `count` (integer, required): Units in the bag after the add.
- `lines` (array, required)
- `total` (number | null, required): Total of the bag with promotions applied, delivery not chosen.
- `offerId` (string, required): The sku of the size added.
- `currency` (string | null, required)
- `subtotal` (number | null, required)
- `productId` (string, required)

## FAQ

### What does "Add a product to the JD Sports cart" do?

Add one size of a product of JD Sports UK (jdsports.co.uk, the United Kingdom store) to the shopping bag of this browser, from its JD Sports product id or product page link and its size (or the size sku from Get JD Sports product), with a quantity, as the product page's size and add to bag buttons do. A product with one size needs no size. Returns the product id, the size sku (offerId), name and size added, the units added, and the bag after the add: each line with its line id, product id, size sku, name, size, quantity, unit price and line price in pounds (GBP), the item count, the total with promotions applied, the subtotal and the currency. Works as a guest, with no account: lines already in the bag stay. Nothing is ordered or paid. An unknown product, a size the product does not have, a size out of stock, or an add the site refuses fails with an error that says so.

### How do I automatically add a product to the JD Sports cart on jdsports.co.uk?

Ask an AI agent connected to Reduck to run reduck/jdsports.co.uk/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/jdsports.co.uk/add_to_cart

### Is there a jdsports.co.uk API to add a product to the JD Sports cart?

You do not need one. "Add a product to the JD Sports cart" drives the real jdsports.co.uk pages in a browser, so it works whether or not jdsports.co.uk offers an API for this.

### What information do I need to provide?

Required: product. Optional: size, offerId, quantity.

### What does it return?

It returns name, size, added, count, lines, total, offerId, currency, subtotal, productId.

### Do I need to be logged in to jdsports.co.uk?

No. It only uses pages of jdsports.co.uk that are reachable without signing in.

### Does it change anything on jdsports.co.uk, or only read data?

It makes changes on jdsports.co.uk, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/jdsports.co.uk/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/jdsports.co.uk/add_to_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/jdsports.co.uk/add_to_cart
