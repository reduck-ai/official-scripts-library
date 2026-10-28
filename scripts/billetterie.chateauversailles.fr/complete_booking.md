# Open the Château de Versailles payment page

Automatically open the Château de Versailles payment page on billetterie.chateauversailles.fr. Take the cart filled with add_to_cart and identified with fill_booking_details on the official Château de Versailles ticket shop to its payment page, and stop there. It never enters payment details and never pays: with dryRun true (the default) it opens the payment form and returns whether it was reached, the total in euros, the payment provider and the cart lines; dryRun false is refused. It ticks the shop's sales conditions box, which the shop asks for before payment. A cart with a total of 0 is confirmed by the shop without payment, so the script stops before that step and says so. An empty cart, or a browser that did not go through fill_booking_details, fails with an error that names the script to run first.

- Site: billetterie.chateauversailles.fr
- Address: `reduck/billetterie.chateauversailles.fr/complete_booking`
- Updated: 2026-10-27 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/billetterie.chateauversailles.fr/complete_booking`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/billetterie.chateauversailles.fr/complete_booking
```

## Input

- `dryRun` (boolean, optional): Stop at the payment page. The script never pays, so false is refused.
- `language` (string, optional)

## Output

- `lines` (array, required)
- `total` (number | null, required)
- `paymentPageReached` (boolean, required)
- `reason` (string | null, optional)
- `paymentHost` (string | null, optional)
- `paymentProvider` (string | null, optional)

## FAQ

### What does "Open the Château de Versailles payment page" do?

Take the cart filled with add_to_cart and identified with fill_booking_details on the official Château de Versailles ticket shop to its payment page, and stop there. It never enters payment details and never pays: with dryRun true (the default) it opens the payment form and returns whether it was reached, the total in euros, the payment provider and the cart lines; dryRun false is refused. It ticks the shop's sales conditions box, which the shop asks for before payment. A cart with a total of 0 is confirmed by the shop without payment, so the script stops before that step and says so. An empty cart, or a browser that did not go through fill_booking_details, fails with an error that names the script to run first.

### How do I automatically open the Château de Versailles payment page on billetterie.chateauversailles.fr?

Ask an AI agent connected to Reduck to run reduck/billetterie.chateauversailles.fr/complete_booking, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/billetterie.chateauversailles.fr/complete_booking

### Is there a billetterie.chateauversailles.fr API to open the Château de Versailles payment page?

You do not need one. "Open the Château de Versailles payment page" drives the real billetterie.chateauversailles.fr pages in a browser, so it works whether or not billetterie.chateauversailles.fr offers an API for this.

### What information do I need to provide?

Optional: dryRun, language.

### What does it return?

It returns lines, total, reason, paymentHost, paymentProvider, paymentPageReached.

### Do I need to be logged in to billetterie.chateauversailles.fr?

No. It only uses pages of billetterie.chateauversailles.fr that are reachable without signing in.

### Does it change anything on billetterie.chateauversailles.fr, or only read data?

It makes changes on billetterie.chateauversailles.fr, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/billetterie.chateauversailles.fr/complete_booking, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/billetterie.chateauversailles.fr/complete_booking

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/billetterie.chateauversailles.fr/complete_booking
