# Add to MediaMarkt Spain cart

Automatically add to MediaMarkt Spain cart on mediamarkt.es. Add a product to the guest shopping cart of this browser on MediaMarkt Spain (mediamarkt.es), by product id or product link, with a quantity from 1 to 10. Returns the cart after the add (number of articles, total in euros, every line) and the product that was added. A product the shop does not sell online, or a link that is not a product page, fails with an error that says so. No sign-in needed; nothing is ordered or paid.

- Site: mediamarkt.es
- Address: `reduck/mediamarkt.es/add_to_cart`
- Updated: 2026-11-24 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/mediamarkt.es/add_to_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/mediamarkt.es/add_to_cart
```

## Input

- `product` (string, required): MediaMarkt Spain product id (the product_id of Search MediaMarkt Spain products), or the product link.
- `quantity` (integer, optional): Number of articles to add.

## Output

- `name` (string | null, required)
- `added` (integer, required): Number of articles added by this run.
- `count` (integer, required)
- `lines` (array, required)
- `total` (number | null, required): Cart total in euros, VAT included, before any shipping cost.
- `offerId` (string | null, required)
- `productId` (string, required): MediaMarkt product id that was added.

## FAQ

### What does "Add to MediaMarkt Spain cart" do?

Add a product to the guest shopping cart of this browser on MediaMarkt Spain (mediamarkt.es), by product id or product link, with a quantity from 1 to 10. Returns the cart after the add (number of articles, total in euros, every line) and the product that was added. A product the shop does not sell online, or a link that is not a product page, fails with an error that says so. No sign-in needed; nothing is ordered or paid.

### How do I automatically add to MediaMarkt Spain cart on mediamarkt.es?

Ask an AI agent connected to Reduck to run reduck/mediamarkt.es/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/mediamarkt.es/add_to_cart

### Is there a mediamarkt.es API to add to MediaMarkt Spain cart?

You do not need one. "Add to MediaMarkt Spain cart" drives the real mediamarkt.es pages in a browser, so it works whether or not mediamarkt.es offers an API for this.

### What information do I need to provide?

Required: product. Optional: quantity.

### What does it return?

It returns name, added, count, lines, total, offerId, productId.

### Do I need to be logged in to mediamarkt.es?

No. It only uses pages of mediamarkt.es that are reachable without signing in.

### Does it change anything on mediamarkt.es, or only read data?

It makes changes on mediamarkt.es, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/mediamarkt.es/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/mediamarkt.es/add_to_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/mediamarkt.es/add_to_cart
