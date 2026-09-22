# Reserve Tickets

Automatically reserve Tickets on ticketmaster.com. Open a Ticketmaster event, select its cheapest listed ticket, set quantity, and click "Reserve Tickets" — holds the seats on a countdown timer, same as clicking through the site by hand. Never proceeds to payment/checkout; stops the moment the reservation lands.

- Site: ticketmaster.com
- Address: `reduck/ticketmaster.com/book_tickets`
- Updated: 2026-09-18 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/ticketmaster.com/book_tickets`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/ticketmaster.com/book_tickets
```

## Input

- `url` (string, required): The event's Ticketmaster URL, from search_events / get_lowest_price.
- `quantity` (integer, optional): How many tickets to reserve. Capped by the site's own event ticket limit.

## Output

- `url` (string, required)
- `currency` (string, required)
- `quantity` (integer, required)
- `subtotal` (number, required)
- `reservedUrl` (string, required): The URL Ticketmaster navigated to after Reserve Tickets was clicked (the timed-hold/checkout page).

## FAQ

### What does "Reserve Tickets" do?

Open a Ticketmaster event, select its cheapest listed ticket, set quantity, and click "Reserve Tickets" — holds the seats on a countdown timer, same as clicking through the site by hand. Never proceeds to payment/checkout; stops the moment the reservation lands.

### How do I automatically reserve Tickets on ticketmaster.com?

Ask an AI agent connected to Reduck to run reduck/ticketmaster.com/book_tickets, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/ticketmaster.com/book_tickets

### Is there a ticketmaster.com API to reserve Tickets?

You do not need one. "Reserve Tickets" drives the real ticketmaster.com pages in a browser, so it works whether or not ticketmaster.com offers an API for this.

### What information do I need to provide?

Required: url. Optional: quantity.

### What does it return?

It returns url, currency, quantity, subtotal, reservedUrl.

### Do I need to be logged in to ticketmaster.com?

Yes. It acts as you on ticketmaster.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the ticketmaster.com cookies saved by the Reduck extension.

### Does it change anything on ticketmaster.com, or only read data?

It makes changes on ticketmaster.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/ticketmaster.com/book_tickets, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/ticketmaster.com/book_tickets

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/ticketmaster.com/book_tickets
