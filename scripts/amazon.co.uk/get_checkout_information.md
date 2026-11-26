# Get Amazon.co.uk checkout information

Automatically get Amazon.co.uk checkout information on amazon.co.uk. Review the checkout of your Amazon.co.uk cart without ordering: recipient, delivery address, payment method, each selected item with its ASIN, quantity and price, the delivery options with their prices, the order summary down to the order total, and a review_hash. Pass address, payment (a card's last 4 digits) and delivery_option to review the checkout with those choices instead of the account's defaults. Pass the review_hash and the same choices to Place Amazon.co.uk order to order exactly this checkout. The cart stays as it is. Fails on an empty cart.

- Site: amazon.co.uk
- Address: `reduck/amazon.co.uk/get_checkout_information`
- Updated: 2026-11-25 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/amazon.co.uk/get_checkout_information`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/amazon.co.uk/get_checkout_information
```

## Input

- `address` (string, optional): The delivery address as the account lists it: the recipient's name, then the address line (for example Jane Doe, 12 Main Street). It must match exactly one of the account's addresses; otherwise the run fails with the list. Omit it to keep Amazon's choice. Pass the same value to the review and to the order.
- `payment` (string, optional): The last 4 digits of the card to pay with. It must match exactly one card of the account; otherwise the run fails with the cards. Omit it to keep Amazon's choice. Pass the same value to the review and to the order.
- `delivery_option` (string, optional): The id of a delivery option from delivery_options of a review, chosen in every delivery group. If a group does not offer it, the run fails with the options offered. Omit it to keep Amazon's choice. Pass the same value to the review and to the order.

## Output

- `groups` (array, required): The checkout's delivery groups: the items that ship together, with their delivery options.
- `totals` (array, required): Order summary lines in page order; the last one is the order total. type is Amazon's own line code, null for the total.
- `review_hash` (string, required): Hash of the recipient, address, payment method, items, selected delivery options and order total shown. Pass it to place the order: the order is placed only while the checkout has the same hash.
- `checkout_url` (string, required): URL of the checkout page that was read.
- `address` (string | null, optional): Delivery address the checkout uses.
- `payment` (string | null, optional): Payment method the checkout uses, as displayed.
- `recipient` (string | null, optional): Who receives the order, as the checkout shows it.
- `order_total` (string | null, optional)

## FAQ

### What does "Get Amazon.co.uk checkout information" do?

Review the checkout of your Amazon.co.uk cart without ordering: recipient, delivery address, payment method, each selected item with its ASIN, quantity and price, the delivery options with their prices, the order summary down to the order total, and a review_hash. Pass address, payment (a card's last 4 digits) and delivery_option to review the checkout with those choices instead of the account's defaults. Pass the review_hash and the same choices to Place Amazon.co.uk order to order exactly this checkout. The cart stays as it is. Fails on an empty cart.

### How do I automatically get Amazon.co.uk checkout information on amazon.co.uk?

Ask an AI agent connected to Reduck to run reduck/amazon.co.uk/get_checkout_information, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/amazon.co.uk/get_checkout_information

### Is there a amazon.co.uk API to get Amazon.co.uk checkout information?

You do not need one. "Get Amazon.co.uk checkout information" drives the real amazon.co.uk pages in a browser, so it works whether or not amazon.co.uk offers an API for this.

### What information do I need to provide?

Optional: address, payment, delivery_option.

### What does it return?

It returns groups, totals, address, payment, recipient, order_total, review_hash, checkout_url.

### Do I need to be logged in to amazon.co.uk?

Yes. It acts as you on amazon.co.uk: in your browser it reuses your session, and on a cloud browser it loads your Auth session cookies for amazon.co.uk.

### Does it change anything on amazon.co.uk, or only read data?

It only reads. It looks things up on amazon.co.uk and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/amazon.co.uk/get_checkout_information, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/amazon.co.uk/get_checkout_information

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/amazon.co.uk/get_checkout_information
