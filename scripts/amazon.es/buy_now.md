# Buy Amazon.es product now

Buy an Amazon.es product by ASIN with Buy Now or Pre-order now, in two steps: review the checkout, then order exactly what you reviewed. It uses the account's default delivery address, payment method and delivery option, or the address, card (payment) and delivery_option you pass. With place_order false (the default) it orders nothing and returns the whole checkout: recipient, delivery address, payment method, the item with its ASIN, quantity and price, the delivery options, the order summary, and a review_hash. To order, run it again with the same product and choices, place_order true and that review_hash: it orders only if the recipient, address, payment method, item, selected delivery option and total are still the same. If one changed, it orders nothing and fails with the checkout as it is now. A checkout left without ordering puts the product in the cart; remove it with Remove Amazon.es product from cart. Returns the order number(s), which Cancel Amazon.es order takes.

- Site: amazon.es
- Address: `reduck/amazon.es/buy_now`
- Updated: 2026-11-25 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/amazon.es/buy_now`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/amazon.es/buy_now
```

## Input

- `asin` (string, required): Product ASIN, e.g. B00NTCH52W.
- `address` (string, optional): The delivery address as the account lists it: the recipient's name, then the address line. It must match exactly one of the account's addresses; otherwise nothing is ordered and the run fails with the list. Omit it to keep Amazon's choice. Pass the same value to the review and to the order.
- `payment` (string, optional): The last 4 digits of the card to pay with. It must match exactly one card of the account; otherwise nothing is ordered and the run fails with the cards. Omit it to keep Amazon's choice. Pass the same value to the review and to the order.
- `quantity` (integer, optional)
- `place_order` (boolean, optional): false: order nothing and return the checkout with its review_hash. true: place the order, which needs review_hash.
- `review_hash` (string, optional): Required with place_order true. The review_hash of the checkout you reviewed. The order is placed only if the checkout still has the same hash; otherwise nothing is ordered and the run fails with the checkout as it is now.
- `delivery_option` (string, optional): The id of a delivery option from delivery_options of a review, chosen in every delivery group. If a group does not offer it, nothing is ordered and the run fails with the options offered. Omit it to keep Amazon's choice. Pass the same value to the review and to the order.

## Output

- `url` (string, required)
- `asin` (string, required)
- `stage` (string, required)
- `groups` (array, required)
- `totals` (array, required)
- `order_ids` (array, required)
- `review_hash` (string, required)
- `checkout_url` (string, required)
- `payment_verification_required` (boolean, required)
- `address` (string | null, optional)
- `payment` (string | null, optional)
- `recipient` (string | null, optional)
- `order_total` (string | null, optional)
- `purchase_id` (string | null, optional)

## FAQ

### What does "Buy Amazon.es product now" do?

Buy an Amazon.es product by ASIN with Buy Now or Pre-order now, in two steps: review the checkout, then order exactly what you reviewed. It uses the account's default delivery address, payment method and delivery option, or the address, card (payment) and delivery_option you pass. With place_order false (the default) it orders nothing and returns the whole checkout: recipient, delivery address, payment method, the item with its ASIN, quantity and price, the delivery options, the order summary, and a review_hash. To order, run it again with the same product and choices, place_order true and that review_hash: it orders only if the recipient, address, payment method, item, selected delivery option and total are still the same. If one changed, it orders nothing and fails with the checkout as it is now. A checkout left without ordering puts the product in the cart; remove it with Remove Amazon.es product from cart. Returns the order number(s), which Cancel Amazon.es order takes.

### What information do I need to provide?

Required: asin. Optional: address, payment, quantity, place_order, review_hash, delivery_option.

### What does it return?

It returns url, asin, stage, groups, totals, address, payment, order_ids, recipient, order_total, purchase_id, review_hash, checkout_url, payment_verification_required.

### Do I need to be logged in to amazon.es?

Yes. It acts as you on amazon.es: in your browser it reuses your session, and on a cloud browser it loads your Auth session cookies for amazon.es.

### Does it change anything on amazon.es, or only read data?

It makes changes on amazon.es, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/amazon.es/buy_now, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/amazon.es/buy_now

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/amazon.es/buy_now
