# Check Château de Versailles ticket availability

Automatically check Château de Versailles ticket availability on billetterie.chateauversailles.fr. For one visit date on the official Château de Versailles ticket shop, list the entry time slots of one ticket type (Passport by default) with the places left in each slot and every rate the slot offers (full, reduced, youth, child, free) with its price in euros. Also lists every ticket type sold that day, so a caller can pick another one by name or id. A day with no entry tickets on sale (for example a Monday, when the palace is closed) returns no slots and a reason. A date in the past or not yet on sale fails with an error. visitors only sets enoughForVisitors on each slot; it reserves nothing.

- Site: billetterie.chateauversailles.fr
- Address: `reduck/billetterie.chateauversailles.fr/check_availability`
- Updated: 2026-10-27 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/billetterie.chateauversailles.fr/check_availability`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/billetterie.chateauversailles.fr/check_availability
```

## Input

- `date` (string, required): Visit date, YYYY-MM-DD.
- `language` (string, optional): Language of the names and rate labels the site returns.
- `visitors` (integer, optional): Number of visitors, used only to set enoughForVisitors on each slot.
- `ticketType` (string, optional): Ticket type: its id or its name, or part of the name, as listed in ticketTypes (552471 is the Passport ticket). A name that matches several types fails with the list of names.

## Output

- `date` (string, required)
- `slots` (array, required)
- `ticketTypes` (array, required)
- `reason` (string | null, optional)
- `ticketType` (object | null, optional)

## FAQ

### What does "Check Château de Versailles ticket availability" do?

For one visit date on the official Château de Versailles ticket shop, list the entry time slots of one ticket type (Passport by default) with the places left in each slot and every rate the slot offers (full, reduced, youth, child, free) with its price in euros. Also lists every ticket type sold that day, so a caller can pick another one by name or id. A day with no entry tickets on sale (for example a Monday, when the palace is closed) returns no slots and a reason. A date in the past or not yet on sale fails with an error. visitors only sets enoughForVisitors on each slot; it reserves nothing.

### How do I automatically check Château de Versailles ticket availability on billetterie.chateauversailles.fr?

Ask an AI agent connected to Reduck to run reduck/billetterie.chateauversailles.fr/check_availability, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/billetterie.chateauversailles.fr/check_availability

### Is there a billetterie.chateauversailles.fr API to check Château de Versailles ticket availability?

You do not need one. "Check Château de Versailles ticket availability" drives the real billetterie.chateauversailles.fr pages in a browser, so it works whether or not billetterie.chateauversailles.fr offers an API for this.

### What information do I need to provide?

Required: date. Optional: language, visitors, ticketType.

### What does it return?

It returns date, slots, reason, ticketType, ticketTypes.

### Do I need to be logged in to billetterie.chateauversailles.fr?

No. It only uses pages of billetterie.chateauversailles.fr that are reachable without signing in.

### Does it change anything on billetterie.chateauversailles.fr, or only read data?

It only reads. It looks things up on billetterie.chateauversailles.fr and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/billetterie.chateauversailles.fr/check_availability, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/billetterie.chateauversailles.fr/check_availability

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/billetterie.chateauversailles.fr/check_availability
