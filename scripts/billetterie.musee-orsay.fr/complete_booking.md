# Open the Musée d'Orsay payment step

Automatically open the Musée d'Orsay payment step on billetterie.musee-orsay.fr. Take the basket filled with add_to_cart, for a buyer identified with fill_booking_details, to the payment step of the official Musée d'Orsay ticket shop, and stop there. It never types card details, never ticks the terms of sale and never clicks the pay button: with dryRun true (the default) it returns whether the payment step was reached, the total in euros, the basket lines, the payment provider and the fields the buyer still has to fill to pay. dryRun false is refused. A basket that is empty, or a buyer the shop has not identified yet, fails with an error that names the step to do first.

- Site: billetterie.musee-orsay.fr
- Address: `reduck/billetterie.musee-orsay.fr/complete_booking`
- Updated: 2026-10-27 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/billetterie.musee-orsay.fr/complete_booking`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/billetterie.musee-orsay.fr/complete_booking
```

## Input

- `dryRun` (boolean, optional): Stop on the payment step. The script never pays, so false is refused.

## Output

- `lines` (array, required)
- `total` (number | null, required)
- `paymentPageReached` (boolean, required)
- `fieldsToPay` (array, optional)
- `paymentHost` (string | null, optional)
- `paymentProvider` (string | null, optional)

## FAQ

### What does "Open the Musée d'Orsay payment step" do?

Take the basket filled with add_to_cart, for a buyer identified with fill_booking_details, to the payment step of the official Musée d'Orsay ticket shop, and stop there. It never types card details, never ticks the terms of sale and never clicks the pay button: with dryRun true (the default) it returns whether the payment step was reached, the total in euros, the basket lines, the payment provider and the fields the buyer still has to fill to pay. dryRun false is refused. A basket that is empty, or a buyer the shop has not identified yet, fails with an error that names the step to do first.

### How do I automatically open the Musée d'Orsay payment step on billetterie.musee-orsay.fr?

Ask an AI agent connected to Reduck to run reduck/billetterie.musee-orsay.fr/complete_booking, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/billetterie.musee-orsay.fr/complete_booking

### Is there a billetterie.musee-orsay.fr API to open the Musée d'Orsay payment step?

You do not need one. "Open the Musée d'Orsay payment step" drives the real billetterie.musee-orsay.fr pages in a browser, so it works whether or not billetterie.musee-orsay.fr offers an API for this.

### What information do I need to provide?

Optional: dryRun.

### What does it return?

It returns lines, total, fieldsToPay, paymentHost, paymentProvider, paymentPageReached.

### Do I need to be logged in to billetterie.musee-orsay.fr?

No. It only uses pages of billetterie.musee-orsay.fr that are reachable without signing in.

### Does it change anything on billetterie.musee-orsay.fr, or only read data?

It only reads. It looks things up on billetterie.musee-orsay.fr and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/billetterie.musee-orsay.fr/complete_booking, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/billetterie.musee-orsay.fr/complete_booking

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/billetterie.musee-orsay.fr/complete_booking
