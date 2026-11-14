# Place a Jewish Museum Berlin ticket order

Place the order for the basket filled with add_to_cart, as the booker given with fill_booking_details, on the official Jewish Museum Berlin ticket shop. With dryRun true (the default) it opens the basket, checks that the order can be placed, and stops before the final "place your binding order" step; nothing is ordered. It returns the basket's reviewHash. With dryRun false and that reviewHash it places the order, which is binding, and the shop emails the tickets; this is only done for a basket whose total is 0, so the script never pays. If the basket changed since the dry run, nothing is ordered and the error gives the current basket and its reviewHash. Returns the basket lines, the total, whether the order was placed, and the order id and the confirmation page the shop gives. An empty basket, or a browser without booking details, fails with an error that names the script to run first.

- Site: tickets.jmberlin.de
- Address: `reduck/tickets.jmberlin.de/pay`
- Updated: 2026-11-13 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/tickets.jmberlin.de/pay`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/tickets.jmberlin.de/pay
```

## Input

- `dryRun` (boolean, optional): Stop before the final step and return the basket's reviewHash. false places a binding order, for a free basket only, and needs that reviewHash.
- `language` (string, optional)
- `reviewHash` (string, optional): The reviewHash a dry run returned for this basket. The order is placed only if the basket still matches it.

## Output

- `lines` (array, required)
- `total` (number, required)
- `ordered` (boolean, required)
- `readyToOrder` (boolean, required)
- `orderId` (string | null, optional)
- `reviewHash` (string, optional): Hash of the basket's tickets, slots, quantities, prices and total.
- `confirmationUrl` (string | null, optional)

## FAQ

### What does "Place a Jewish Museum Berlin ticket order" do?

Place the order for the basket filled with add_to_cart, as the booker given with fill_booking_details, on the official Jewish Museum Berlin ticket shop. With dryRun true (the default) it opens the basket, checks that the order can be placed, and stops before the final "place your binding order" step; nothing is ordered. It returns the basket's reviewHash. With dryRun false and that reviewHash it places the order, which is binding, and the shop emails the tickets; this is only done for a basket whose total is 0, so the script never pays. If the basket changed since the dry run, nothing is ordered and the error gives the current basket and its reviewHash. Returns the basket lines, the total, whether the order was placed, and the order id and the confirmation page the shop gives. An empty basket, or a browser without booking details, fails with an error that names the script to run first.

### What information do I need to provide?

Optional: dryRun, language, reviewHash.

### What does it return?

It returns lines, total, orderId, ordered, reviewHash, readyToOrder, confirmationUrl.

### Do I need to be logged in to tickets.jmberlin.de?

No. It only uses pages of tickets.jmberlin.de that are reachable without signing in.

### Does it change anything on tickets.jmberlin.de, or only read data?

It makes changes on tickets.jmberlin.de, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/tickets.jmberlin.de/pay, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/tickets.jmberlin.de/pay

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/tickets.jmberlin.de/pay
