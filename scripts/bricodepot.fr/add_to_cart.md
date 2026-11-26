# Add Brico Depot product to cart

Automatically add Brico Depot product to cart on bricodepot.fr. Add a Brico Depot (bricodepot.fr) product to the shopping cart of this browser from its sku or product page link, with a quantity from 1 to 10, and return the cart as the site holds it afterwards: the item count, the items total in euros (taxes included) and each line with its line id, product id (the sku), offer id (always null), name, seller (always Brico Dépôt), quantity, unit price and line price. Works as a guest, with no account: the cart lives in the browser, so lines already in it stay and are listed too. A Brico Depot cart belongs to one depot: pass a depot id from Search Brico Depot depots, or leave it out to use the depot the cart or the browser already has. A product the depot cannot sell (out of stock, not enough units) fails with an error that says so, and so does a sku the site does not know or a link that is not a product page. Nothing is paid or ordered.

- Site: bricodepot.fr
- Address: `reduck/bricodepot.fr/add_to_cart`
- Updated: 2026-11-25 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/bricodepot.fr/add_to_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/bricodepot.fr/add_to_cart
```

## Input

- `product` (string, required): Sku from Search Brico Depot products (for example 5063022538369), or a product page link such as https://www.bricodepot.fr/p/5063022538369/ruban-adhesif-d-emballage-66-m-marron.
- `depot_id` (integer, optional): Depot of the cart, the depot_id returned by Search Brico Depot depots. Needed when the cart and the browser have no depot yet.
- `quantity` (integer, optional): How many units to add.

## Output

- `name` (string | null, required)
- `added` (integer, required): Units this run added.
- `count` (integer, required): Units in the cart.
- `lines` (array, required)
- `total` (number | null, required): Items total in euros, taxes included, delivery not included.
- `offerId` (string | null, required)
- `productId` (string, required)

## FAQ

### What does "Add Brico Depot product to cart" do?

Add a Brico Depot (bricodepot.fr) product to the shopping cart of this browser from its sku or product page link, with a quantity from 1 to 10, and return the cart as the site holds it afterwards: the item count, the items total in euros (taxes included) and each line with its line id, product id (the sku), offer id (always null), name, seller (always Brico Dépôt), quantity, unit price and line price. Works as a guest, with no account: the cart lives in the browser, so lines already in it stay and are listed too. A Brico Depot cart belongs to one depot: pass a depot id from Search Brico Depot depots, or leave it out to use the depot the cart or the browser already has. A product the depot cannot sell (out of stock, not enough units) fails with an error that says so, and so does a sku the site does not know or a link that is not a product page. Nothing is paid or ordered.

### How do I automatically add Brico Depot product to cart on bricodepot.fr?

Ask an AI agent connected to Reduck to run reduck/bricodepot.fr/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/bricodepot.fr/add_to_cart

### Is there a bricodepot.fr API to add Brico Depot product to cart?

You do not need one. "Add Brico Depot product to cart" drives the real bricodepot.fr pages in a browser, so it works whether or not bricodepot.fr offers an API for this.

### What information do I need to provide?

Required: product. Optional: depot_id, quantity.

### What does it return?

It returns name, added, count, lines, total, offerId, productId.

### Do I need to be logged in to bricodepot.fr?

No. It only uses pages of bricodepot.fr that are reachable without signing in.

### Does it change anything on bricodepot.fr, or only read data?

It makes changes on bricodepot.fr, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/bricodepot.fr/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/bricodepot.fr/add_to_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/bricodepot.fr/add_to_cart
