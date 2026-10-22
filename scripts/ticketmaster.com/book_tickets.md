# Reserve Ticketmaster tickets

Automatically reserve Ticketmaster tickets on ticketmaster.com. Reserve tickets for a Ticketmaster event: returns the quantity held, the subtotal in USD and the link to Ticketmaster's timed hold page. Nothing is paid; the hold expires on its own if not completed. Fails with a signed-out error when the browser is not signed in to Ticketmaster, and says so when the event offers no tickets (over, sold out, not yet on sale), only code-locked presale offers, or not the quantity asked.

- Site: ticketmaster.com
- Address: `reduck/ticketmaster.com/book_tickets`
- Updated: 2026-10-21 (v7)
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

### What does "Reserve Ticketmaster tickets" do?

Reserve tickets for a Ticketmaster event: returns the quantity held, the subtotal in USD and the link to Ticketmaster's timed hold page. Nothing is paid; the hold expires on its own if not completed. Fails with a signed-out error when the browser is not signed in to Ticketmaster, and says so when the event offers no tickets (over, sold out, not yet on sale), only code-locked presale offers, or not the quantity asked.

### How do I automatically reserve Ticketmaster tickets on ticketmaster.com?

Ask an AI agent connected to Reduck to run reduck/ticketmaster.com/book_tickets, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/ticketmaster.com/book_tickets

### Is there a ticketmaster.com API to reserve Ticketmaster tickets?

You do not need one. "Reserve Ticketmaster tickets" drives the real ticketmaster.com pages in a browser, so it works whether or not ticketmaster.com offers an API for this.

### What information do I need to provide?

Required: url. Optional: quantity.

### What does it return?

It returns url, currency, quantity, subtotal, reservedUrl.

### Do I need to be logged in to ticketmaster.com?

Yes. It acts as you on ticketmaster.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the ticketmaster.com cookies saved by the Reduck extension.

### Does it change anything on ticketmaster.com, or only read data?

It makes changes on ticketmaster.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/ticketmaster.com/book_tickets, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/ticketmaster.com/book_tickets

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/ticketmaster.com/book_tickets
