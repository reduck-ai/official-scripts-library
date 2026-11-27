# Add a product to the Athleta cart

Automatically add a product to the Athleta cart on athleta.gap.com. Add a size of an Athleta US (athleta.gap.com) product to the shopping bag of this browser, for shipping, and return the bag as the site holds it afterwards. Give the product id or link and the offerId of the size, both from Get Athleta product, and a quantity from 1 to 5. Returns the product id, offer id, name, the number of units added, and the bag: the number of units, the estimated total before tax and shipping, and each line with its line id, product id, offer id, name, seller, quantity, unit price and line price in US dollars. Athleta can show units of one size on several lines, for example when an offer prices them differently. Works as a guest, with no account: lines already in the bag stay and are listed too. Nothing is paid or ordered. A product that Athleta does not know, a missing or unknown offerId, an out of stock size, or a quantity out of range fails with a message that says so, and adds nothing.

- Site: athleta.gap.com
- Address: `reduck/athleta.gap.com/add_to_cart`
- Updated: 2026-11-26 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/athleta.gap.com/add_to_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/athleta.gap.com/add_to_cart
```

## Input

- `productId` (string, required): Athleta product id, color id or product page link, as returned by Search Athleta products or Get Athleta product.
- `offerId` (string, optional): The sku of the size to add, from the variants of Get Athleta product. Needed when the product has more than one size.
- `quantity` (integer, optional): Number of units to add, 1 to 5.

## Output

- `name` (string | null, required)
- `added` (integer, required)
- `count` (integer, required)
- `lines` (array, required)
- `total` (number | null, required)
- `offerId` (string, required)
- `productId` (string, required)

## FAQ

### What does "Add a product to the Athleta cart" do?

Add a size of an Athleta US (athleta.gap.com) product to the shopping bag of this browser, for shipping, and return the bag as the site holds it afterwards. Give the product id or link and the offerId of the size, both from Get Athleta product, and a quantity from 1 to 5. Returns the product id, offer id, name, the number of units added, and the bag: the number of units, the estimated total before tax and shipping, and each line with its line id, product id, offer id, name, seller, quantity, unit price and line price in US dollars. Athleta can show units of one size on several lines, for example when an offer prices them differently. Works as a guest, with no account: lines already in the bag stay and are listed too. Nothing is paid or ordered. A product that Athleta does not know, a missing or unknown offerId, an out of stock size, or a quantity out of range fails with a message that says so, and adds nothing.

### How do I automatically add a product to the Athleta cart on athleta.gap.com?

Ask an AI agent connected to Reduck to run reduck/athleta.gap.com/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/athleta.gap.com/add_to_cart

### Is there a athleta.gap.com API to add a product to the Athleta cart?

You do not need one. "Add a product to the Athleta cart" drives the real athleta.gap.com pages in a browser, so it works whether or not athleta.gap.com offers an API for this.

### What information do I need to provide?

Required: productId. Optional: offerId, quantity.

### What does it return?

It returns name, added, count, lines, total, offerId, productId.

### Do I need to be logged in to athleta.gap.com?

No. It only uses pages of athleta.gap.com that are reachable without signing in.

### Does it change anything on athleta.gap.com, or only read data?

It makes changes on athleta.gap.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/athleta.gap.com/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/athleta.gap.com/add_to_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/athleta.gap.com/add_to_cart
