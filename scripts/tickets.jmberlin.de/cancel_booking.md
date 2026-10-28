# Cancel a free Jewish Museum Berlin order

Automatically cancel a free Jewish Museum Berlin order on tickets.jmberlin.de. Cancel a free order placed on the official Jewish Museum Berlin ticket shop, from the order link in its booking confirmation email. Pass the order number too, to make sure the link opens that order. Returns the order number and cancelled when the shop confirms it, or no_cancel_option when the order page offers no cancellation (an order already cancelled, or a paid order, which the museum's terms do not let a visitor cancel). Cancelling cannot be undone, and the tickets go back on sale.

- Site: tickets.jmberlin.de
- Address: `reduck/tickets.jmberlin.de/cancel_booking`
- Updated: 2026-10-27 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/tickets.jmberlin.de/cancel_booking`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/tickets.jmberlin.de/cancel_booking
```

## Input

- `orderUrl` (string, required): The order link from the booking confirmation email (https://jmb.gomus.de/public/v1/order/...).
- `orderNumber` (string, required): The order number from the email subject, checked against the page before cancelling.

## Output

- `status` (string, required)
- `orderNumber` (string, required)

## FAQ

### What does "Cancel a free Jewish Museum Berlin order" do?

Cancel a free order placed on the official Jewish Museum Berlin ticket shop, from the order link in its booking confirmation email. Pass the order number too, to make sure the link opens that order. Returns the order number and cancelled when the shop confirms it, or no_cancel_option when the order page offers no cancellation (an order already cancelled, or a paid order, which the museum's terms do not let a visitor cancel). Cancelling cannot be undone, and the tickets go back on sale.

### How do I automatically cancel a free Jewish Museum Berlin order on tickets.jmberlin.de?

Ask an AI agent connected to Reduck to run reduck/tickets.jmberlin.de/cancel_booking, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/tickets.jmberlin.de/cancel_booking

### Is there a tickets.jmberlin.de API to cancel a free Jewish Museum Berlin order?

You do not need one. "Cancel a free Jewish Museum Berlin order" drives the real tickets.jmberlin.de pages in a browser, so it works whether or not tickets.jmberlin.de offers an API for this.

### What information do I need to provide?

Required: orderUrl, orderNumber.

### What does it return?

It returns status, orderNumber.

### Do I need to be logged in to tickets.jmberlin.de?

No. It only uses pages of tickets.jmberlin.de that are reachable without signing in.

### Does it change anything on tickets.jmberlin.de, or only read data?

It makes changes on tickets.jmberlin.de, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/tickets.jmberlin.de/cancel_booking, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/tickets.jmberlin.de/cancel_booking

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/tickets.jmberlin.de/cancel_booking
