# List Uber trips

Automatically list Uber trips on riders.uber.com. List the signed-in rider's past Uber trips (riders.uber.com/trips), newest first. Returns per trip: tripId (uuid), title (destination address), when (e.g. "Jul 10 • 10:50 PM"), amount (e.g. "€12.98"), url. Loads more trips until max is reached or the list runs out. tripId is the join key for riders.uber.com/download_invoice.

- Site: riders.uber.com
- Address: `reduck/riders.uber.com/list_trips`
- Updated: 2026-09-21 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/riders.uber.com/list_trips`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/riders.uber.com/list_trips
```

## Input

- `max` (integer, optional): Maximum trips to return (default 20).

## Output

- `total` (integer, required)
- `trips` (array, required)

## FAQ

### What does "List Uber trips" do?

List the signed-in rider's past Uber trips (riders.uber.com/trips), newest first. Returns per trip: tripId (uuid), title (destination address), when (e.g. "Jul 10 • 10:50 PM"), amount (e.g. "€12.98"), url. Loads more trips until max is reached or the list runs out. tripId is the join key for riders.uber.com/download_invoice.

### How do I automatically list Uber trips on riders.uber.com?

Ask an AI agent connected to Reduck to run reduck/riders.uber.com/list_trips, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/riders.uber.com/list_trips

### Is there a riders.uber.com API to list Uber trips?

You do not need one. "List Uber trips" drives the real riders.uber.com pages in a browser, so it works whether or not riders.uber.com offers an API for this.

### What information do I need to provide?

Optional: max.

### What does it return?

It returns total, trips.

### Do I need to be logged in to riders.uber.com?

Yes. It acts as you on riders.uber.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the riders.uber.com cookies saved by the Reduck extension.

### Does it change anything on riders.uber.com, or only read data?

It only reads. It looks things up on riders.uber.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/riders.uber.com/list_trips, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/riders.uber.com/list_trips

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/riders.uber.com/list_trips
