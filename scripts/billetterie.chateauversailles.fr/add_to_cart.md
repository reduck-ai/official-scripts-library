# Add Château de Versailles tickets to the cart

Automatically add Château de Versailles tickets to the cart on billetterie.chateauversailles.fr. Put tickets for one date, one entry slot and one ticket type (Passport by default) in the cart of the official Château de Versailles ticket shop, with a quantity per rate (full, reduced, youth, child, free). Take the slot and the rates from check_availability: a slot is its slotId or its time (HH:MM), a rate is its priceId or its label. Returns the cart lines (date, slot time, entrance, ticket, rate, quantity, unit price, line total), the cart total in euros and how many seconds the site still holds the cart. The cart lives in this browser: tickets already in it stay there and are listed too. The site holds a cart for about 35 minutes. Nothing is paid or booked. A quantity above what the slot allows, an unknown slot or an unknown rate fails with an error that names the valid ones.

- Site: billetterie.chateauversailles.fr
- Address: `reduck/billetterie.chateauversailles.fr/add_to_cart`
- Updated: 2026-10-27 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/billetterie.chateauversailles.fr/add_to_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/billetterie.chateauversailles.fr/add_to_cart
```

## Input

- `date` (string, required): Visit date, YYYY-MM-DD.
- `slot` (string, required): Entry slot: its slotId or its time (HH:MM), from check_availability.
- `tickets` (array, required): Quantity per visitor category.
- `language` (string, optional): Language of the labels the site returns. Rate labels must be in this language.
- `ticketType` (string, optional): Ticket type id or name, as in check_availability (552471 is the Passport ticket).

## Output

- `cart` (object, required)
- `added` (array, required)

## FAQ

### What does "Add Château de Versailles tickets to the cart" do?

Put tickets for one date, one entry slot and one ticket type (Passport by default) in the cart of the official Château de Versailles ticket shop, with a quantity per rate (full, reduced, youth, child, free). Take the slot and the rates from check_availability: a slot is its slotId or its time (HH:MM), a rate is its priceId or its label. Returns the cart lines (date, slot time, entrance, ticket, rate, quantity, unit price, line total), the cart total in euros and how many seconds the site still holds the cart. The cart lives in this browser: tickets already in it stay there and are listed too. The site holds a cart for about 35 minutes. Nothing is paid or booked. A quantity above what the slot allows, an unknown slot or an unknown rate fails with an error that names the valid ones.

### How do I automatically add Château de Versailles tickets to the cart on billetterie.chateauversailles.fr?

Ask an AI agent connected to Reduck to run reduck/billetterie.chateauversailles.fr/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/billetterie.chateauversailles.fr/add_to_cart

### Is there a billetterie.chateauversailles.fr API to add Château de Versailles tickets to the cart?

You do not need one. "Add Château de Versailles tickets to the cart" drives the real billetterie.chateauversailles.fr pages in a browser, so it works whether or not billetterie.chateauversailles.fr offers an API for this.

### What information do I need to provide?

Required: date, slot, tickets. Optional: language, ticketType.

### What does it return?

It returns cart, added.

### Do I need to be logged in to billetterie.chateauversailles.fr?

No. It only uses pages of billetterie.chateauversailles.fr that are reachable without signing in.

### Does it change anything on billetterie.chateauversailles.fr, or only read data?

It makes changes on billetterie.chateauversailles.fr, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/billetterie.chateauversailles.fr/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/billetterie.chateauversailles.fr/add_to_cart

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/billetterie.chateauversailles.fr/add_to_cart
