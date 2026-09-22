# Book SNCF Connect train ticket (cart only, cancellable fares)

Automatically book SNCF Connect train ticket (cart only, cancellable fares) on sncf-connect.com. An unofficial SNCF Connect API: put a train ticket in your SNCF Connect cart programmatically, from code or from an AI agent, with typed JSON in and out. SNCF Connect has no public booking API.

- Site: sncf-connect.com
- Address: `reduck/sncf-connect.com/book_tickets`
- Updated: 2026-09-16 (v16)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/sncf-connect.com/book_tickets`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/sncf-connect.com/book_tickets
```

## Input

- `date` (string, required): Travel date YYYY-MM-DD. Must not be in the past.
- `origin` (string, required): Departure city or station
- `destination` (string, required): Arrival city or station
- `comfortClass` (string, optional): Comfort class filter (default 2de)
- `flexibleOnly` (boolean, optional): If true, only fully-flexible fares (no exchange/refund fee) are eligible, not merely refundable-until-J-7 ones
- `departureTime` (string, optional): Optional HH:MM to pick a specific train; omit to take the cheapest eligible fare across all trains

## Output

- `fare` (object, required)
- `note` (string, required)
- `journey` (object, required)
- `addedToCart` (boolean, required)
- `priceValidUntil` (string | null, optional): Cart price validity deadline as shown (e.g. '14:11'); the cart keeps items 15-30 min

## FAQ

### What does "Book SNCF Connect train ticket (cart only, cancellable fares)" do?

Add a train ticket to the SNCF Connect cart — never proceeds to payment, stopping right after the ticket lands in the cart. Safety gate: only fares cancellable or refundable free of charge at booking time are eligible. Picks the cheapest eligible fare of the requested comfort class, on the train matching departureTime (or the cheapest eligible across all trains if omitted). Requires login. Runs only via the local browser extension, not the hosted cloud browser.

### How do I automatically book SNCF Connect train ticket (cart only, cancellable fares) on sncf-connect.com?

Ask an AI agent connected to Reduck to run reduck/sncf-connect.com/book_tickets, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/sncf-connect.com/book_tickets

### Is there a sncf-connect.com API to book SNCF Connect train ticket (cart only, cancellable fares)?

You do not need one. "Book SNCF Connect train ticket (cart only, cancellable fares)" drives the real sncf-connect.com pages in a browser, so it works whether or not sncf-connect.com offers an API for this.

### What information do I need to provide?

Required: origin, destination, date. Optional: comfortClass, flexibleOnly, departureTime.

### What does it return?

It returns fare, note, journey, addedToCart, priceValidUntil.

### Do I need to be logged in to sncf-connect.com?

No. It only uses pages of sncf-connect.com that are reachable without signing in.

### Does it change anything on sncf-connect.com, or only read data?

It makes changes on sncf-connect.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/sncf-connect.com/book_tickets, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/sncf-connect.com/book_tickets

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/sncf-connect.com/book_tickets
