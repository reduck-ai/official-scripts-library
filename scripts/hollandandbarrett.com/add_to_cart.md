# Add a product to the Holland & Barrett cart

Automatically add a product to the Holland & Barrett cart on hollandandbarrett.com. Add a product of Holland & Barrett UK (hollandandbarrett.com, the United Kingdom store) to the basket of this browser, from its Holland & Barrett product id or product page link, with a quantity, as the product page's add to basket button does. Each size of a product has its own product id (see sizes in Get Holland & Barrett product). Returns the product id, its sku (offerId) and name, the units added, and the basket after the add: each line with its product id, sku, name, seller, quantity, unit price and line price in pounds (GBP), the item count, the total and the currency. Works as a guest, with no account: lines already in the basket stay. Nothing is ordered or paid. An unknown product, a product page with no add button, or an add the site refuses fails with an error that says so.

- Site: hollandandbarrett.com
- Address: `reduck/hollandandbarrett.com/add_to_cart`
- Updated: 2026-11-27 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/hollandandbarrett.com/add_to_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/hollandandbarrett.com/add_to_cart
```

## Input

- `product` (string, required): A Holland & Barrett product id as Search Holland & Barrett products returns it, for example 6100005252, or a hollandandbarrett.com product page link.
- `quantity` (integer, optional): How many units to add.

## Output

- `name` (string | null, required)
- `added` (integer, required): Units this run added.
- `count` (integer, required): Units in the basket after the add.
- `lines` (array, required)
- `total` (number | null, required): Total of the basket with promotions applied, delivery not included.
- `offerId` (string, required): The sku of the product added.
- `currency` (string | null, required)
- `productId` (string, required)

## FAQ

### What does "Add a product to the Holland & Barrett cart" do?

Add a product of Holland & Barrett UK (hollandandbarrett.com, the United Kingdom store) to the basket of this browser, from its Holland & Barrett product id or product page link, with a quantity, as the product page's add to basket button does. Each size of a product has its own product id (see sizes in Get Holland & Barrett product). Returns the product id, its sku (offerId) and name, the units added, and the basket after the add: each line with its product id, sku, name, seller, quantity, unit price and line price in pounds (GBP), the item count, the total and the currency. Works as a guest, with no account: lines already in the basket stay. Nothing is ordered or paid. An unknown product, a product page with no add button, or an add the site refuses fails with an error that says so.

### How do I automatically add a product to the Holland & Barrett cart on hollandandbarrett.com?

Ask an AI agent connected to Reduck to run reduck/hollandandbarrett.com/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/hollandandbarrett.com/add_to_cart

### Is there a hollandandbarrett.com API to add a product to the Holland & Barrett cart?

You do not need one. "Add a product to the Holland & Barrett cart" drives the real hollandandbarrett.com pages in a browser, so it works whether or not hollandandbarrett.com offers an API for this.

### What information do I need to provide?

Required: product. Optional: quantity.

### What does it return?

It returns name, added, count, lines, total, offerId, currency, productId.

### Do I need to be logged in to hollandandbarrett.com?

No. It only uses pages of hollandandbarrett.com that are reachable without signing in.

### Does it change anything on hollandandbarrett.com, or only read data?

It makes changes on hollandandbarrett.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/hollandandbarrett.com/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/hollandandbarrett.com/add_to_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/hollandandbarrett.com/add_to_cart
