# Remove a product from the SATURN cart

Automatically remove a product from the SATURN cart on saturn.de. Remove one line from the guest shopping cart of this browser on SATURN Germany (saturn.de, the German store), by product id or product link, whatever its quantity. When the cart holds the product from more than one seller, pass offer_id (the offerId of List SATURN cart items) to say which line; offer_id "saturn" picks the line SATURN sells. Returns the cart after the removal (number of articles, total and currency, every line) and removed true; a product that is not in the cart leaves the cart as it is and returns removed false. Other lines are never touched. No sign-in needed.

- Site: saturn.de
- Address: `reduck/saturn.de/remove_from_cart`
- Updated: 2026-11-26 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/saturn.de/remove_from_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/saturn.de/remove_from_cart
```

## Input

- `product` (string, required): SATURN product id as List SATURN cart items gives it (productId), or the product link.
- `offer_id` (string, optional): The offerId of the line to remove, as List SATURN cart items gives it, or saturn for the line SATURN sells. Needed only when the cart holds the product from more than one seller.

## Output

- `count` (integer, required): Number of articles in the cart after the removal.
- `lines` (array, required)
- `total` (number | null, required): Cart total, VAT included, before any shipping cost the checkout adds.
- `removed` (boolean, required): True when the line was in the cart and is now gone.
- `currency` (string | null, required): Currency of the prices, EUR.

## FAQ

### What does "Remove a product from the SATURN cart" do?

Remove one line from the guest shopping cart of this browser on SATURN Germany (saturn.de, the German store), by product id or product link, whatever its quantity. When the cart holds the product from more than one seller, pass offer_id (the offerId of List SATURN cart items) to say which line; offer_id "saturn" picks the line SATURN sells. Returns the cart after the removal (number of articles, total and currency, every line) and removed true; a product that is not in the cart leaves the cart as it is and returns removed false. Other lines are never touched. No sign-in needed.

### How do I automatically remove a product from the SATURN cart on saturn.de?

Ask an AI agent connected to Reduck to run reduck/saturn.de/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/saturn.de/remove_from_cart

### Is there a saturn.de API to remove a product from the SATURN cart?

You do not need one. "Remove a product from the SATURN cart" drives the real saturn.de pages in a browser, so it works whether or not saturn.de offers an API for this.

### What information do I need to provide?

Required: product. Optional: offer_id.

### What does it return?

It returns count, lines, total, removed, currency.

### Do I need to be logged in to saturn.de?

No. It only uses pages of saturn.de that are reachable without signing in.

### Does it change anything on saturn.de, or only read data?

It makes changes on saturn.de, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/saturn.de/remove_from_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/saturn.de/remove_from_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/saturn.de/remove_from_cart
