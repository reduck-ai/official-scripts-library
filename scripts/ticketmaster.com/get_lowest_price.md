# Get Ticketmaster event lowest ticket price

Automatically get Ticketmaster event lowest ticket price on ticketmaster.com. Open a Ticketmaster event page and return the lowest listed ticket price (Ticketmaster's own default "lowest price first" ticket list ordering) plus currency. Fails with a signed-out error when the browser is not signed in to Ticketmaster, and with an error when the event shows no ticket list (cancelled, sold out or off sale).

- Site: ticketmaster.com
- Address: `reduck/ticketmaster.com/get_lowest_price`
- Updated: 2026-10-29 (v5)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/ticketmaster.com/get_lowest_price`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/ticketmaster.com/get_lowest_price
```

## Input

- `url` (string, required): The event's Ticketmaster URL, from search_events.

## Output

- `url` (string, required)
- `currency` (string, required)
- `lowestPrice` (number, required)

## FAQ

### What does "Get Ticketmaster event lowest ticket price" do?

Open a Ticketmaster event page and return the lowest listed ticket price (Ticketmaster's own default "lowest price first" ticket list ordering) plus currency. Fails with a signed-out error when the browser is not signed in to Ticketmaster, and with an error when the event shows no ticket list (cancelled, sold out or off sale).

### How do I automatically get Ticketmaster event lowest ticket price on ticketmaster.com?

Ask an AI agent connected to Reduck to run reduck/ticketmaster.com/get_lowest_price, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/ticketmaster.com/get_lowest_price

### Is there a ticketmaster.com API to get Ticketmaster event lowest ticket price?

You do not need one. "Get Ticketmaster event lowest ticket price" drives the real ticketmaster.com pages in a browser, so it works whether or not ticketmaster.com offers an API for this.

### What information do I need to provide?

Required: url.

### What does it return?

It returns url, currency, lowestPrice.

### Do I need to be logged in to ticketmaster.com?

Yes. It acts as you on ticketmaster.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the ticketmaster.com cookies saved by the Reduck extension.

### Does it change anything on ticketmaster.com, or only read data?

It only reads. It looks things up on ticketmaster.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/ticketmaster.com/get_lowest_price, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/ticketmaster.com/get_lowest_price

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/ticketmaster.com/get_lowest_price
