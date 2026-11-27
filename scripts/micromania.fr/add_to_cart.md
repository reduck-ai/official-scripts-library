# Add a product to the Micromania cart

Automatically add a product to the Micromania cart on micromania.fr. Add a Micromania product to the shopping cart from its product page link, with an optional quantity, and return the cart as the site holds it afterwards: each line with its product id, name, quantity, unit price and line price in euros, plus the item count and the total of the items. Works as a guest, with no account: the cart lives in the browser, so lines already in it stay and are listed too. Nothing is paid or ordered. A product page without the add button (out of stock, in store only) fails with an error, and so does a quantity above what the site allows per cart; a link that is not a Micromania product page fails with an error.

- Site: micromania.fr
- Address: `reduck/micromania.fr/add_to_cart`
- Updated: 2026-11-24 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/micromania.fr/add_to_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/micromania.fr/add_to_cart
```

## Input

- `url` (string, required): Link of a Micromania product page, as Search Micromania products returns it in url, such as https://www.micromania.fr/p/booster-pokemon-blade-awakening-chinois-158402.html.
- `quantity` (integer, optional): How many units to add to the cart. The site caps the units per product (often 4 to 6).

## Output

- `name` (string | null, required)
- `added` (integer, required): Units this run added to the cart.
- `count` (integer, required): Units in the cart after the add.
- `lines` (array, required)
- `total` (number | null, required): Total of the items in euros, delivery not included.
- `offerId` (string | null, required)
- `productId` (string, required)

## FAQ

### What does "Add a product to the Micromania cart" do?

Add a Micromania product to the shopping cart from its product page link, with an optional quantity, and return the cart as the site holds it afterwards: each line with its product id, name, quantity, unit price and line price in euros, plus the item count and the total of the items. Works as a guest, with no account: the cart lives in the browser, so lines already in it stay and are listed too. Nothing is paid or ordered. A product page without the add button (out of stock, in store only) fails with an error, and so does a quantity above what the site allows per cart; a link that is not a Micromania product page fails with an error.

### How do I automatically add a product to the Micromania cart on micromania.fr?

Ask an AI agent connected to Reduck to run reduck/micromania.fr/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/micromania.fr/add_to_cart

### Is there a micromania.fr API to add a product to the Micromania cart?

You do not need one. "Add a product to the Micromania cart" drives the real micromania.fr pages in a browser, so it works whether or not micromania.fr offers an API for this.

### What information do I need to provide?

Required: url. Optional: quantity.

### What does it return?

It returns name, added, count, lines, total, offerId, productId.

### Do I need to be logged in to micromania.fr?

No. It only uses pages of micromania.fr that are reachable without signing in.

### Does it change anything on micromania.fr, or only read data?

It makes changes on micromania.fr, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/micromania.fr/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/micromania.fr/add_to_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/micromania.fr/add_to_cart
