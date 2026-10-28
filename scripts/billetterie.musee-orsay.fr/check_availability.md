# Check Musée d'Orsay timed-entry availability

Automatically check Musée d'Orsay timed-entry availability on billetterie.musee-orsay.fr. For one visit date on the official Musée d'Orsay ticket shop, list the timed-entry slots of one ticket offer (the standard timed admission by default) and whether each slot can still be booked, plus the rates with their prices in euros and the most one order can hold, read from the first slot that can be booked. The shop does not show how many places a slot has left, only whether it is bookable. A day with no slot on sale (for example a Monday, when the museum is closed) returns no slots and a reason.

- Site: billetterie.musee-orsay.fr
- Address: `reduck/billetterie.musee-orsay.fr/check_availability`
- Updated: 2026-10-27 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/billetterie.musee-orsay.fr/check_availability`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/billetterie.musee-orsay.fr/check_availability
```

## Input

- `date` (string, required): Visit date, YYYY-MM-DD.
- `eventId` (integer, optional): Ticket offer id in the shop: 1100509 is the standard timed admission to the museum.
- `language` (string, optional): Language of the rate labels.

## Output

- `date` (string, required)
- `slots` (array, required)
- `prices` (array, required)
- `event` (string | null, optional)
- `reason` (string | null, optional)
- `eventId` (integer, optional)
- `pricesFromSlotId` (string | null, optional)

## FAQ

### What does "Check Musée d'Orsay timed-entry availability" do?

For one visit date on the official Musée d'Orsay ticket shop, list the timed-entry slots of one ticket offer (the standard timed admission by default) and whether each slot can still be booked, plus the rates with their prices in euros and the most one order can hold, read from the first slot that can be booked. The shop does not show how many places a slot has left, only whether it is bookable. A day with no slot on sale (for example a Monday, when the museum is closed) returns no slots and a reason.

### How do I automatically check Musée d'Orsay timed-entry availability on billetterie.musee-orsay.fr?

Ask an AI agent connected to Reduck to run reduck/billetterie.musee-orsay.fr/check_availability, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/billetterie.musee-orsay.fr/check_availability

### Is there a billetterie.musee-orsay.fr API to check Musée d'Orsay timed-entry availability?

You do not need one. "Check Musée d'Orsay timed-entry availability" drives the real billetterie.musee-orsay.fr pages in a browser, so it works whether or not billetterie.musee-orsay.fr offers an API for this.

### What information do I need to provide?

Required: date. Optional: eventId, language.

### What does it return?

It returns date, event, slots, prices, reason, eventId, pricesFromSlotId.

### Do I need to be logged in to billetterie.musee-orsay.fr?

No. It only uses pages of billetterie.musee-orsay.fr that are reachable without signing in.

### Does it change anything on billetterie.musee-orsay.fr, or only read data?

It only reads. It looks things up on billetterie.musee-orsay.fr and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/billetterie.musee-orsay.fr/check_availability, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/billetterie.musee-orsay.fr/check_availability

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/billetterie.musee-orsay.fr/check_availability
