# Get Amazon.es checkout information

Automatically get Amazon.es checkout information on amazon.es. Review the checkout of your Amazon.es cart without ordering: recipient, delivery address, payment method, each selected item with its ASIN, quantity and price, the delivery options with their prices, the order summary down to the order total, and a review_hash. Pass address, payment (a card's last 4 digits) and delivery_option to review the checkout with those choices instead of the account's defaults. The cart stays as it is. Fails on an empty cart.

- Site: amazon.es
- Address: `reduck/amazon.es/get_checkout_information`
- Updated: 2026-11-25 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/amazon.es/get_checkout_information`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/amazon.es/get_checkout_information
```

## Input

- `address` (string, optional): The delivery address as the account lists it: the recipient's name, then the address line. It must match exactly one of the account's addresses; otherwise the run fails with the list. Omit it to keep Amazon's choice.
- `payment` (string, optional): The last 4 digits of the card to pay with. It must match exactly one card of the account; otherwise the run fails with the cards. Omit it to keep Amazon's choice.
- `delivery_option` (string, optional): The id of a delivery option from delivery_options of a review, chosen in every delivery group. If a group does not offer it, the run fails with the options offered. Omit it to keep Amazon's choice.

## Output

- `groups` (array, required)
- `totals` (array, required)
- `review_hash` (string, required): Hash of the recipient, address, payment method, items, selected delivery options and order total shown.
- `checkout_url` (string, required)
- `address` (string | null, optional)
- `payment` (string | null, optional)
- `recipient` (string | null, optional)
- `order_total` (string | null, optional)

## FAQ

### What does "Get Amazon.es checkout information" do?

Review the checkout of your Amazon.es cart without ordering: recipient, delivery address, payment method, each selected item with its ASIN, quantity and price, the delivery options with their prices, the order summary down to the order total, and a review_hash. Pass address, payment (a card's last 4 digits) and delivery_option to review the checkout with those choices instead of the account's defaults. The cart stays as it is. Fails on an empty cart.

### How do I automatically get Amazon.es checkout information on amazon.es?

Ask an AI agent connected to Reduck to run reduck/amazon.es/get_checkout_information, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/amazon.es/get_checkout_information

### Is there a amazon.es API to get Amazon.es checkout information?

You do not need one. "Get Amazon.es checkout information" drives the real amazon.es pages in a browser, so it works whether or not amazon.es offers an API for this.

### What information do I need to provide?

Optional: address, payment, delivery_option.

### What does it return?

It returns groups, totals, address, payment, recipient, order_total, review_hash, checkout_url.

### Do I need to be logged in to amazon.es?

Yes. It acts as you on amazon.es: in your browser it reuses your session, and on a cloud browser it loads your Auth session cookies for amazon.es.

### Does it change anything on amazon.es, or only read data?

It only reads. It looks things up on amazon.es and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/amazon.es/get_checkout_information, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/amazon.es/get_checkout_information

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/amazon.es/get_checkout_information
