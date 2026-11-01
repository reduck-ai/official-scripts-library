# Get Amazon.fr checkout information

Automatically get Amazon.fr checkout information on amazon.fr. Review an Amazon.fr checkout before placing the order: delivery address, payment method, items, delivery options with their prices, and the order summary down to the order total. It reads the checkout page open in the current session, so run it in the same session after Buy Amazon product now or Check out Amazon cart stopped at checkout; it does not open a checkout by itself.

- Site: amazon.fr
- Address: `reduck/amazon.fr/get_checkout_information`
- Updated: 2026-10-31 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/amazon.fr/get_checkout_information`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/amazon.fr/get_checkout_information
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

### What does "Get Amazon.fr checkout information" do?

Review an Amazon.fr checkout before placing the order: delivery address, payment method, items, delivery options with their prices, and the order summary down to the order total. It reads the checkout page open in the current session, so run it in the same session after Buy Amazon product now or Check out Amazon cart stopped at checkout; it does not open a checkout by itself.

### How do I automatically get Amazon.fr checkout information on amazon.fr?

Ask an AI agent connected to Reduck to run reduck/amazon.fr/get_checkout_information, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/amazon.fr/get_checkout_information

### Is there a amazon.fr API to get Amazon.fr checkout information?

You do not need one. "Get Amazon.fr checkout information" drives the real amazon.fr pages in a browser, so it works whether or not amazon.fr offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns groups, totals, address, payment, recipient, order_total, checkout_url.

### Do I need to be logged in to amazon.fr?

Yes. It acts as you on amazon.fr: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the amazon.fr cookies saved by the Reduck extension.

### Does it change anything on amazon.fr, or only read data?

It only reads. It looks things up on amazon.fr and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/amazon.fr/get_checkout_information, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/amazon.fr/get_checkout_information

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/amazon.fr/get_checkout_information
