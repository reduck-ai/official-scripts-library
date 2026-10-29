# Check Jewish Museum Berlin ticket availability

Automatically check Jewish Museum Berlin ticket availability on tickets.jmberlin.de. For one visit date on the official Jewish Museum Berlin ticket shop, list the entry time slots of one ticket type (adults by default) for one exhibition (the core exhibition by default), with the places left and the slot's total places, plus every ticket type sold for that exhibition that day with its price in euros and the most one order can hold. A day that is not on sale (in the past, too far ahead, or closed) returns no slots and a reason. Pass time (HH:MM) to get only that slot, with available and, when it cannot be booked, the reason (full, not on sale, or no entry at that time) instead of an error; the shop shows past, too-far-ahead and closed days the same way, so all three come back as not on sale.

- Site: tickets.jmberlin.de
- Address: `reduck/tickets.jmberlin.de/check_availability`
- Updated: 2026-10-28 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/tickets.jmberlin.de/check_availability`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/tickets.jmberlin.de/check_availability
```

## Input

- `date` (string, required): Visit date, YYYY-MM-DD.
- `time` (string, optional): Entry time, HH:MM (24-hour). When given, only that slot is returned, with available and, when it cannot be booked, unavailableReason and reason instead of an error.
- `language` (string, optional)
- `visitors` (integer, optional): Number of visitors, used only to set enoughForVisitors on each slot.
- `ticketType` (string, optional): Ticket type: its id or a part of its title, as listed in ticketTypes (177 is the core exhibition adult ticket).
- `exhibitionId` (integer, optional): Exhibition id in the shop: 11 is the core exhibition.

## Output

- `date` (string, required)
- `slots` (array, required)
- `ticketTypes` (array, required)
- `reason` (string | null, optional)
- `available` (boolean | null, optional): With time: whether that slot can be booked. Null without time.
- `ticketType` (object | null, optional)
- `unavailableReason` (string | null, optional): With time, when the slot cannot be booked: full, not_on_sale (the shop sells no ticket that day: past, too far ahead or closed; it does not say which) or no_slot_at_time. Null otherwise.

## FAQ

### What does "Check Jewish Museum Berlin ticket availability" do?

For one visit date on the official Jewish Museum Berlin ticket shop, list the entry time slots of one ticket type (adults by default) for one exhibition (the core exhibition by default), with the places left and the slot's total places, plus every ticket type sold for that exhibition that day with its price in euros and the most one order can hold. A day that is not on sale (in the past, too far ahead, or closed) returns no slots and a reason. Pass time (HH:MM) to get only that slot, with available and, when it cannot be booked, the reason (full, not on sale, or no entry at that time) instead of an error; the shop shows past, too-far-ahead and closed days the same way, so all three come back as not on sale.

### How do I automatically check Jewish Museum Berlin ticket availability on tickets.jmberlin.de?

Ask an AI agent connected to Reduck to run reduck/tickets.jmberlin.de/check_availability, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/tickets.jmberlin.de/check_availability

### Is there a tickets.jmberlin.de API to check Jewish Museum Berlin ticket availability?

You do not need one. "Check Jewish Museum Berlin ticket availability" drives the real tickets.jmberlin.de pages in a browser, so it works whether or not tickets.jmberlin.de offers an API for this.

### What information do I need to provide?

Required: date. Optional: time, language, visitors, ticketType, exhibitionId.

### What does it return?

It returns date, slots, reason, available, ticketType, ticketTypes, unavailableReason.

### Do I need to be logged in to tickets.jmberlin.de?

No. It only uses pages of tickets.jmberlin.de that are reachable without signing in.

### Does it change anything on tickets.jmberlin.de, or only read data?

It only reads. It looks things up on tickets.jmberlin.de and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/tickets.jmberlin.de/check_availability, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/tickets.jmberlin.de/check_availability

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/tickets.jmberlin.de/check_availability
