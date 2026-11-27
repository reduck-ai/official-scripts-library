# Remove a product from the Banana Republic cart

Automatically remove a product from the Banana Republic cart on bananarepublic.gap.com. Remove lines from the Banana Republic US (bananarepublic.gap.com) shopping bag of this browser and return the bag as the site holds it afterwards. Give lineId to remove one line, or offerId to remove every line of that size. Both come from List the items in the Banana Republic cart. Returns removed (true when lines were removed, false when no line matched, and then nothing is changed), the number of units, the estimated total before tax and shipping, and each line left with its line id, product id, offer id, name, seller, quantity, unit price and line price in US dollars. Works as a guest, with no account.

- Site: bananarepublic.gap.com
- Address: `reduck/bananarepublic.gap.com/remove_from_cart`
- Updated: 2026-11-26 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/bananarepublic.gap.com/remove_from_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/bananarepublic.gap.com/remove_from_cart
```

## Input

- `lineId` (string, optional): Line id of one bag line, from List the items in the Banana Republic cart. Give lineId or offerId.
- `offerId` (string, optional): The sku of a size in the bag: every line of it is removed. Give lineId or offerId.

## Output

- `count` (integer, required)
- `lines` (array, required)
- `total` (number | null, required)
- `removed` (boolean, required)

## FAQ

### What does "Remove a product from the Banana Republic cart" do?

Remove lines from the Banana Republic US (bananarepublic.gap.com) shopping bag of this browser and return the bag as the site holds it afterwards. Give lineId to remove one line, or offerId to remove every line of that size. Both come from List the items in the Banana Republic cart. Returns removed (true when lines were removed, false when no line matched, and then nothing is changed), the number of units, the estimated total before tax and shipping, and each line left with its line id, product id, offer id, name, seller, quantity, unit price and line price in US dollars. Works as a guest, with no account.

### How do I automatically remove a product from the Banana Republic cart on bananarepublic.gap.com?

Ask an AI agent connected to Reduck to run reduck/bananarepublic.gap.com/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/bananarepublic.gap.com/remove_from_cart

### Is there a bananarepublic.gap.com API to remove a product from the Banana Republic cart?

You do not need one. "Remove a product from the Banana Republic cart" drives the real bananarepublic.gap.com pages in a browser, so it works whether or not bananarepublic.gap.com offers an API for this.

### What information do I need to provide?

Optional: lineId, offerId.

### What does it return?

It returns count, lines, total, removed.

### Do I need to be logged in to bananarepublic.gap.com?

No. It only uses pages of bananarepublic.gap.com that are reachable without signing in.

### Does it change anything on bananarepublic.gap.com, or only read data?

It makes changes on bananarepublic.gap.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/bananarepublic.gap.com/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/bananarepublic.gap.com/remove_from_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/bananarepublic.gap.com/remove_from_cart
