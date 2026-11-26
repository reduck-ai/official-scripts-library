# Place Amazon.es order from checkout

Order your Amazon.es cart as you reviewed it, and get the order number(s), to track the order or cancel it. Takes the review_hash from Get Amazon.es checkout information, and the same address, payment and delivery_option you reviewed with. It opens the cart's checkout again, applies those choices, and orders only if it still has the same recipient, address, payment method, items, selected delivery options and total. If one changed, it orders nothing and fails with the checkout as it is now, so you can check it and pass its new review_hash. Returns the order number(s) from Your Orders, the checkout it ordered, and whether the card issuer asked for a payment verification. This spends money.

- Site: amazon.es
- Address: `reduck/amazon.es/place_order`
- Updated: 2026-11-25 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/amazon.es/place_order`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/amazon.es/place_order
```

## Input

- `review_hash` (string, required): The review_hash of the checkout you reviewed. The order is placed only if the checkout still has the same hash; otherwise nothing is ordered and the run fails with the checkout as it is now.
- `address` (string, optional): The delivery address as the account lists it: the recipient's name, then the address line. It must match exactly one of the account's addresses; otherwise nothing is ordered and the run fails with the list. Omit it to keep Amazon's choice. Pass the same value to the review and to the order.
- `payment` (string, optional): The last 4 digits of the card to pay with. It must match exactly one card of the account; otherwise nothing is ordered and the run fails with the cards. Omit it to keep Amazon's choice. Pass the same value to the review and to the order.
- `delivery_option` (string, optional): The id of a delivery option from delivery_options of a review, chosen in every delivery group. If a group does not offer it, nothing is ordered and the run fails with the options offered. Omit it to keep Amazon's choice. Pass the same value to the review and to the order.

## Output

- `groups` (array, required)
- `totals` (array, required)
- `order_ids` (array, required): Order numbers created by this purchase, as shown in Your Orders. Pass one to Cancel Amazon.es order.
- `review_hash` (string, required)
- `checkout_url` (string, required)
- `confirmation_url` (string, required)
- `payment_verification_required` (boolean, required): True when the card issuer asked the cardholder to verify the payment instead of showing the confirmation page. The order exists but waits for that approval.
- `address` (string | null, optional)
- `payment` (string | null, optional)
- `recipient` (string | null, optional)
- `order_total` (string | null, optional)
- `purchase_id` (string | null, optional)

## FAQ

### What does "Place Amazon.es order from checkout" do?

Order your Amazon.es cart as you reviewed it, and get the order number(s), to track the order or cancel it. Takes the review_hash from Get Amazon.es checkout information, and the same address, payment and delivery_option you reviewed with. It opens the cart's checkout again, applies those choices, and orders only if it still has the same recipient, address, payment method, items, selected delivery options and total. If one changed, it orders nothing and fails with the checkout as it is now, so you can check it and pass its new review_hash. Returns the order number(s) from Your Orders, the checkout it ordered, and whether the card issuer asked for a payment verification. This spends money.

### What information do I need to provide?

Required: review_hash. Optional: address, payment, delivery_option.

### What does it return?

It returns groups, totals, address, payment, order_ids, recipient, order_total, purchase_id, review_hash, checkout_url, confirmation_url, payment_verification_required.

### Do I need to be logged in to amazon.es?

Yes. It acts as you on amazon.es: in your browser it reuses your session, and on a cloud browser it loads your Auth session cookies for amazon.es.

### Does it change anything on amazon.es, or only read data?

It makes changes on amazon.es, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/amazon.es/place_order, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/amazon.es/place_order

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/amazon.es/place_order
