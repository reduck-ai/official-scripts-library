# List booked tickets (future / past / pending options)

Automatically list booked tickets (future / past / pending options) on sncf-connect.com. List the account's booked tickets from SNCF Connect "Billets > Vos voyages": upcoming trips, past trips, and pending free options (pre-reservations). SNCF Connect exposes no "cancelled tickets" list — a cancelled trip simply disappears; this is a site limitation, not a filter. Requires login. Runs only via the local browser extension, not the hosted cloud browser.

- Site: sncf-connect.com
- Address: `reduck/sncf-connect.com/list_tickets`
- Updated: 2026-09-08 (v4)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/sncf-connect.com/list_tickets`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/sncf-connect.com/list_tickets
```

## Input

- `scope` (string, optional): Which lists to fetch. 'future' also returns pending options; 'past' skips them.

## Output

- `note` (string, required)
- `past` (array, required)
- `future` (array, required)
- `options` (array, required)

## Example output

Shape only: placeholder values generated from the output schema, not a real run.

```json
{
  "note": "…",
  "past": [
    "…"
  ],
  "future": [
    "…"
  ],
  "options": [
    "…"
  ]
}
```

## FAQ

### What does "List booked tickets (future / past / pending options)" do?

List the account's booked tickets from SNCF Connect "Billets > Vos voyages": upcoming trips, past trips, and pending free options (pre-reservations). SNCF Connect exposes no "cancelled tickets" list — a cancelled trip simply disappears; this is a site limitation, not a filter. Requires login. Runs only via the local browser extension, not the hosted cloud browser.

### How do I automatically list booked tickets (future / past / pending options) on sncf-connect.com?

Ask an AI agent connected to Reduck to run reduck/sncf-connect.com/list_tickets, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/sncf-connect.com/list_tickets

### Is there a sncf-connect.com API to list booked tickets (future / past / pending options)?

You do not need one. "List booked tickets (future / past / pending options)" drives the real sncf-connect.com pages in a browser, so it works whether or not sncf-connect.com offers an API for this.

### What information do I need to provide?

Optional: scope.

### What does it return?

It returns note, past, future, options.

### Do I need to be logged in to sncf-connect.com?

Yes. It acts as you on sncf-connect.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the sncf-connect.com cookies saved by the Reduck extension.

### Does it change anything on sncf-connect.com, or only read data?

It only reads. It looks things up on sncf-connect.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/sncf-connect.com/list_tickets, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/sncf-connect.com/list_tickets

### Who maintains it?

It is part of Reduck's official curated catalogue.

### Is there a SNCF Connect API to list your booked SNCF Connect tickets?

Not an official one you can use for this: SNCF Connect has no public API for a traveller's tickets. This script works as an unofficial SNCF Connect API for it: typed input, JSON output, callable from an AI agent over MCP, from the CLI, or over REST.

### How do I list your booked SNCF Connect tickets programmatically?

Call this script with its arguments and read the JSON it returns. It drives SNCF Connect in a real browser session, so there is no API key to request and nothing to reverse-engineer yourself.

Source: https://reduck.ai/explore/scripts/reduck/sncf-connect.com/list_tickets
