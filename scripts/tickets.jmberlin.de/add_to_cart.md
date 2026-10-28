# Add Jewish Museum Berlin tickets to the basket

Automatically add Jewish Museum Berlin tickets to the basket on tickets.jmberlin.de. Put tickets for one date and one entry slot in the basket of the official Jewish Museum Berlin ticket shop, with a quantity per ticket type (adults, under age of 18). Take the slot and the ticket types from check_availability: a slot is its time (HH:MM) or its startsAt value, a ticket type is its id or a part of its title. Returns the basket lines (ticket, slot, quantity, unit price, line total) and the total in euros. The basket lives in this browser: tickets already in it stay, unless emptyBasketFirst is true. Nothing is booked until complete_booking places the order. A slot with too few places, an unknown slot or ticket type, or a quantity above the most one order can hold fails with an error that names the valid values.

- Site: tickets.jmberlin.de
- Address: `reduck/tickets.jmberlin.de/add_to_cart`
- Updated: 2026-10-27 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/tickets.jmberlin.de/add_to_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/tickets.jmberlin.de/add_to_cart
```

## Input

- `date` (string, required): Visit date, YYYY-MM-DD.
- `slot` (string, required): Entry slot: its time (HH:MM) or its startsAt value, from check_availability.
- `tickets` (array, required): Quantity per ticket type.
- `language` (string, optional)
- `exhibitionId` (integer, optional): Exhibition id in the shop: 11 is the core exhibition.
- `emptyBasketFirst` (boolean, optional): Remove what the basket holds before adding these tickets.

## Output

- `added` (array, required)
- `basket` (object, required)

## FAQ

### What does "Add Jewish Museum Berlin tickets to the basket" do?

Put tickets for one date and one entry slot in the basket of the official Jewish Museum Berlin ticket shop, with a quantity per ticket type (adults, under age of 18). Take the slot and the ticket types from check_availability: a slot is its time (HH:MM) or its startsAt value, a ticket type is its id or a part of its title. Returns the basket lines (ticket, slot, quantity, unit price, line total) and the total in euros. The basket lives in this browser: tickets already in it stay, unless emptyBasketFirst is true. Nothing is booked until complete_booking places the order. A slot with too few places, an unknown slot or ticket type, or a quantity above the most one order can hold fails with an error that names the valid values.

### How do I automatically add Jewish Museum Berlin tickets to the basket on tickets.jmberlin.de?

Ask an AI agent connected to Reduck to run reduck/tickets.jmberlin.de/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/tickets.jmberlin.de/add_to_cart

### Is there a tickets.jmberlin.de API to add Jewish Museum Berlin tickets to the basket?

You do not need one. "Add Jewish Museum Berlin tickets to the basket" drives the real tickets.jmberlin.de pages in a browser, so it works whether or not tickets.jmberlin.de offers an API for this.

### What information do I need to provide?

Required: date, slot, tickets. Optional: language, exhibitionId, emptyBasketFirst.

### What does it return?

It returns added, basket.

### Do I need to be logged in to tickets.jmberlin.de?

No. It only uses pages of tickets.jmberlin.de that are reachable without signing in.

### Does it change anything on tickets.jmberlin.de, or only read data?

It makes changes on tickets.jmberlin.de, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/tickets.jmberlin.de/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/tickets.jmberlin.de/add_to_cart

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/tickets.jmberlin.de/add_to_cart
