# Add Musée d'Orsay timed-entry tickets to the basket

Automatically add Musée d'Orsay timed-entry tickets to the basket on billetterie.musee-orsay.fr. Put tickets for one date and one timed-entry slot in the basket of the official Musée d'Orsay ticket shop, with a quantity per rate. Take the slot and the rates from check_availability: a slot is its slotId or its time (HH:MM), a rate is its priceId or its label. Returns the basket lines (event, date and time, rate, quantity, unit price), the total in euros and how many seconds the shop still holds the basket (about 15 minutes). Tickets already in the basket stay. Nothing is paid or booked. A slot that is full, an unknown slot or rate, or a quantity above what the slot allows fails with an error that names the valid values.

- Site: billetterie.musee-orsay.fr
- Address: `reduck/billetterie.musee-orsay.fr/add_to_cart`
- Updated: 2026-10-27 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/billetterie.musee-orsay.fr/add_to_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/billetterie.musee-orsay.fr/add_to_cart
```

## Input

- `date` (string, required): Visit date, YYYY-MM-DD.
- `slot` (string, required): Entry slot: its slotId or its time (HH:MM), from check_availability.
- `tickets` (array, required)
- `eventId` (integer, optional): Ticket offer id: 1100509 is the standard timed admission to the museum.
- `language` (string, optional)

## Output

- `added` (array, required)
- `basket` (object, required)

## FAQ

### What does "Add Musée d'Orsay timed-entry tickets to the basket" do?

Put tickets for one date and one timed-entry slot in the basket of the official Musée d'Orsay ticket shop, with a quantity per rate. Take the slot and the rates from check_availability: a slot is its slotId or its time (HH:MM), a rate is its priceId or its label. Returns the basket lines (event, date and time, rate, quantity, unit price), the total in euros and how many seconds the shop still holds the basket (about 15 minutes). Tickets already in the basket stay. Nothing is paid or booked. A slot that is full, an unknown slot or rate, or a quantity above what the slot allows fails with an error that names the valid values.

### How do I automatically add Musée d'Orsay timed-entry tickets to the basket on billetterie.musee-orsay.fr?

Ask an AI agent connected to Reduck to run reduck/billetterie.musee-orsay.fr/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/billetterie.musee-orsay.fr/add_to_cart

### Is there a billetterie.musee-orsay.fr API to add Musée d'Orsay timed-entry tickets to the basket?

You do not need one. "Add Musée d'Orsay timed-entry tickets to the basket" drives the real billetterie.musee-orsay.fr pages in a browser, so it works whether or not billetterie.musee-orsay.fr offers an API for this.

### What information do I need to provide?

Required: date, slot, tickets. Optional: eventId, language.

### What does it return?

It returns added, basket.

### Do I need to be logged in to billetterie.musee-orsay.fr?

No. It only uses pages of billetterie.musee-orsay.fr that are reachable without signing in.

### Does it change anything on billetterie.musee-orsay.fr, or only read data?

It makes changes on billetterie.musee-orsay.fr, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/billetterie.musee-orsay.fr/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/billetterie.musee-orsay.fr/add_to_cart

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/billetterie.musee-orsay.fr/add_to_cart
