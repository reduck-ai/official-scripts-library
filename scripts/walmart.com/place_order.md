# Place Walmart order from checkout

Place the order on an open Walmart.com checkout and get its order number. It places the checkout open in the current session as it stands (address, payment method, items), so run it in the same session after Check out Walmart cart stopped on the review page. Returns the order number, the order total Walmart confirmed and the confirmation page URL. This spends money. Walmart can still cancel a placed order afterwards (for example for unusual account activity); its order page then says so and nothing is charged. Walmart sometimes refuses automated checkout steps with its "Robot or human?" check; the run then fails saying so (nothing is ordered when it refuses the order request), and it usually clears after a pause.

- Site: walmart.com
- Address: `reduck/walmart.com/place_order`
- Updated: 2026-10-27 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/walmart.com/place_order`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/walmart.com/place_order
```

## Input

It takes no input.

## Output

- `order_id` (string, required): Walmart's order number, as Purchase history shows it.
- `confirmation_url` (string, required)
- `order_total` (string | null, optional): Order total on the confirmation, as Walmart displays it.

## FAQ

### What does "Place Walmart order from checkout" do?

Place the order on an open Walmart.com checkout and get its order number. It places the checkout open in the current session as it stands (address, payment method, items), so run it in the same session after Check out Walmart cart stopped on the review page. Returns the order number, the order total Walmart confirmed and the confirmation page URL. This spends money. Walmart can still cancel a placed order afterwards (for example for unusual account activity); its order page then says so and nothing is charged. Walmart sometimes refuses automated checkout steps with its "Robot or human?" check; the run then fails saying so (nothing is ordered when it refuses the order request), and it usually clears after a pause.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns order_id, order_total, confirmation_url.

### Do I need to be logged in to walmart.com?

Yes. It acts as you on walmart.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the walmart.com cookies saved by the Reduck extension.

### Does it change anything on walmart.com, or only read data?

It makes changes on walmart.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/walmart.com/place_order, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/walmart.com/place_order

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/walmart.com/place_order
