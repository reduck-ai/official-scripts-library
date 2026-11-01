# Get Amazon.de checkout information

Automatically get Amazon.de checkout information on amazon.de. Review an Amazon.de checkout before placing the order: delivery address, payment method, items, delivery options with their prices, and the order summary down to the order total. It reads the checkout page open in the current session, so run it in the same session after Buy Amazon product now or Check out Amazon cart stopped at checkout; it does not open a checkout by itself.

- Site: amazon.de
- Address: `reduck/amazon.de/get_checkout_information`
- Updated: 2026-10-31 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/amazon.de/get_checkout_information`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/amazon.de/get_checkout_information
```

## Input

It takes no input.

## Output

- `groups` (array, required)
- `totals` (array, required): Order summary lines in page order; the last one is the order total. type is Amazon's own line code (e.g. ITEMS_TAX_EXCLUSIVE), null for the total.
- `checkout_url` (string, required)
- `address` (string | null, optional)
- `payment` (string | null, optional)
- `recipient` (string | null, optional)
- `order_total` (string | null, optional)

## FAQ

### What does "Get Amazon.de checkout information" do?

Review an Amazon.de checkout before placing the order: delivery address, payment method, items, delivery options with their prices, and the order summary down to the order total. It reads the checkout page open in the current session, so run it in the same session after Buy Amazon product now or Check out Amazon cart stopped at checkout; it does not open a checkout by itself.

### How do I automatically get Amazon.de checkout information on amazon.de?

Ask an AI agent connected to Reduck to run reduck/amazon.de/get_checkout_information, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/amazon.de/get_checkout_information

### Is there a amazon.de API to get Amazon.de checkout information?

You do not need one. "Get Amazon.de checkout information" drives the real amazon.de pages in a browser, so it works whether or not amazon.de offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns groups, totals, address, payment, recipient, order_total, checkout_url.

### Do I need to be logged in to amazon.de?

Yes. It acts as you on amazon.de: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the amazon.de cookies saved by the Reduck extension.

### Does it change anything on amazon.de, or only read data?

It only reads. It looks things up on amazon.de and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/amazon.de/get_checkout_information, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/amazon.de/get_checkout_information

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/amazon.de/get_checkout_information
