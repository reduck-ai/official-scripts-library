# Buy Amazon.de product now

Buy an Amazon.de product by ASIN with Buy Now or Pre-order now: stop at checkout to review it first, or place the order at once. It uses the account's default delivery address and payment method, confirming the preselected address when Amazon asks for one. By default it stops on the checkout page without ordering and returns the order total, address and payment method; to review and then place that checkout, run it in a session and follow with Get Amazon checkout information and Place Amazon order. A checkout left without ordering puts the product in the cart; remove it with Remove Amazon product from cart. With place_order set to true it places the order at once and returns the order number(s), which Cancel Amazon order takes.

- Site: amazon.de
- Address: `reduck/amazon.de/buy_now`
- Updated: 2026-10-31 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/amazon.de/buy_now`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/amazon.de/buy_now
```

## Input

- `asin` (string, required): Product ASIN, e.g. 0008612102.
- `quantity` (integer, optional)
- `place_order` (boolean, optional): false: stop on the checkout page without ordering. To review and then place that checkout, run this inside a session (start_session, then pass its sessionId to this run and to Get Amazon checkout information and Place Amazon order); without a session the checkout page closes with the run. true: place the order immediately.

## Output

- `url` (string, required): Checkout page URL (stage checkout), or the confirmation or payment verification page URL (stage ordered).
- `asin` (string, required)
- `stage` (string, required)
- `order_ids` (array, required): Order numbers created by this purchase (stage ordered), as shown in Your Orders. Pass one to Cancel Amazon order.
- `payment_verification_required` (boolean, required): True when the card issuer asked the cardholder to verify the payment (for example in their bank app) instead of showing the confirmation page. The order exists but waits for that approval.
- `address` (string | null, optional): Delivery address the checkout uses.
- `payment` (string | null, optional): Payment method the checkout uses, as displayed (e.g. Paying with Mastercard 1234).
- `order_total` (string | null, optional)
- `purchase_id` (string | null, optional): Amazon's id for the checkout itself (stage ordered); not an order number.

## FAQ

### What does "Buy Amazon.de product now" do?

Buy an Amazon.de product by ASIN with Buy Now or Pre-order now: stop at checkout to review it first, or place the order at once. It uses the account's default delivery address and payment method, confirming the preselected address when Amazon asks for one. By default it stops on the checkout page without ordering and returns the order total, address and payment method; to review and then place that checkout, run it in a session and follow with Get Amazon checkout information and Place Amazon order. A checkout left without ordering puts the product in the cart; remove it with Remove Amazon product from cart. With place_order set to true it places the order at once and returns the order number(s), which Cancel Amazon order takes.

### What information do I need to provide?

Required: asin. Optional: quantity, place_order.

### What does it return?

It returns url, asin, stage, address, payment, order_ids, order_total, purchase_id, payment_verification_required.

### Do I need to be logged in to amazon.de?

Yes. It acts as you on amazon.de: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the amazon.de cookies saved by the Reduck extension.

### Does it change anything on amazon.de, or only read data?

It makes changes on amazon.de, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/amazon.de/buy_now, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/amazon.de/buy_now

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/amazon.de/buy_now
