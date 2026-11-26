# Check out Amazon.co.uk cart

Automatically check out Amazon.co.uk cart on amazon.co.uk. Check out your Amazon.co.uk shopping cart in two steps: review the checkout, then order exactly what you reviewed. It checks out the selected cart items with the account's default delivery address, payment method and delivery option, or with the address, card (payment) and delivery_option you pass. With place_order false (the default) it orders nothing and returns the whole checkout: recipient, delivery address, payment method, each item with its ASIN, quantity and price, the delivery options, the order summary, and a review_hash. To order, run it again with place_order true, that review_hash and the same choices: it opens the checkout again and orders only if the recipient, address, payment method, items, selected delivery options and total are still the same. If one changed, it orders nothing and fails with the checkout as it is now, so you can check it and pass its new review_hash. Returns the order number(s), which Cancel Amazon.co.uk order takes. Fails on an empty cart.

- Site: amazon.co.uk
- Address: `reduck/amazon.co.uk/checkout_cart`
- Updated: 2026-11-25 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/amazon.co.uk/checkout_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/amazon.co.uk/checkout_cart
```

## Input

- `address` (string, optional): The delivery address as the account lists it: the recipient's name, then the address line (for example Jane Doe, 12 Main Street). It must match exactly one of the account's addresses; otherwise nothing is ordered and the run fails with the list. Omit it to keep Amazon's choice. Pass the same value to the review and to the order.
- `payment` (string, optional): The last 4 digits of the card to pay with. It must match exactly one card of the account; otherwise nothing is ordered and the run fails with the cards. Omit it to keep Amazon's choice. Pass the same value to the review and to the order.
- `place_order` (boolean, optional): false: order nothing and return the checkout with its review_hash. true: place the order, which needs review_hash.
- `review_hash` (string, optional): Required with place_order true. The review_hash of the checkout you reviewed. The order is placed only if the checkout still has the same hash; otherwise nothing is ordered and the run fails with the checkout as it is now.
- `delivery_option` (string, optional): The id of a delivery option from delivery_options of a review, chosen in every delivery group. If a group does not offer it, nothing is ordered and the run fails with the options offered. Omit it to keep Amazon's choice. Pass the same value to the review and to the order.

## Output

- `url` (string, required): Checkout page URL (stage checkout), or the confirmation or payment verification page URL (stage ordered).
- `stage` (string, required)
- `groups` (array, required)
- `totals` (array, required)
- `order_ids` (array, required): Order numbers created by this purchase, as shown in Your Orders. Pass one to Cancel Amazon.co.uk order.
- `review_hash` (string, required)
- `checkout_url` (string, required)
- `payment_verification_required` (boolean, required): True when the card issuer asked the cardholder to verify the payment instead of showing the confirmation page. The order exists but waits for that approval.
- `address` (string | null, optional)
- `payment` (string | null, optional)
- `recipient` (string | null, optional)
- `order_total` (string | null, optional)
- `purchase_id` (string | null, optional): Amazon's id for the checkout itself; not an order number.

## FAQ

### What does "Check out Amazon.co.uk cart" do?

Check out your Amazon.co.uk shopping cart in two steps: review the checkout, then order exactly what you reviewed. It checks out the selected cart items with the account's default delivery address, payment method and delivery option, or with the address, card (payment) and delivery_option you pass. With place_order false (the default) it orders nothing and returns the whole checkout: recipient, delivery address, payment method, each item with its ASIN, quantity and price, the delivery options, the order summary, and a review_hash. To order, run it again with place_order true, that review_hash and the same choices: it opens the checkout again and orders only if the recipient, address, payment method, items, selected delivery options and total are still the same. If one changed, it orders nothing and fails with the checkout as it is now, so you can check it and pass its new review_hash. Returns the order number(s), which Cancel Amazon.co.uk order takes. Fails on an empty cart.

### How do I automatically check out Amazon.co.uk cart on amazon.co.uk?

Ask an AI agent connected to Reduck to run reduck/amazon.co.uk/checkout_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/amazon.co.uk/checkout_cart

### Is there a amazon.co.uk API to check out Amazon.co.uk cart?

You do not need one. "Check out Amazon.co.uk cart" drives the real amazon.co.uk pages in a browser, so it works whether or not amazon.co.uk offers an API for this.

### What information do I need to provide?

Optional: address, payment, place_order, review_hash, delivery_option.

### What does it return?

It returns url, stage, groups, totals, address, payment, order_ids, recipient, order_total, purchase_id, review_hash, checkout_url, payment_verification_required.

### Do I need to be logged in to amazon.co.uk?

Yes. It acts as you on amazon.co.uk: in your browser it reuses your session, and on a cloud browser it loads your Auth session cookies for amazon.co.uk.

### Does it change anything on amazon.co.uk, or only read data?

It makes changes on amazon.co.uk, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/amazon.co.uk/checkout_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/amazon.co.uk/checkout_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/amazon.co.uk/checkout_cart
