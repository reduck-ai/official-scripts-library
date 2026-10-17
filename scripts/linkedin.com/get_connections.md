# Get LinkedIn connections

Automatically get LinkedIn connections on linkedin.com. Your own 1st-degree LinkedIn connections as rows with headline, profile URL, member URN and connected-on text.

- Site: linkedin.com
- Address: `reduck/linkedin.com/get_connections`
- Updated: 2026-10-16 (v7)
- Author: Reduck AI (reduck)

## About

The run opens the Connections page under My Network in the signed-in browser and scrolls the list until no new cards appear for about 6 seconds, or until your count is reached. It returns whatever is in the page at that point, so a slow lazy load can end the run with a partial list and no error. Compare connections.length with total to spot a gap, and run again if it matters. Key your spreadsheet on memberUrn rather than publicId, because people rename their vanity URL and the URN stays put. connectedOnText is LinkedIn's own line in your display language, so parse it yourself before sorting by date. There is no email, location or separate company field, and the headline is whatever each person typed. Large networks take a while, since every card must load on a single scrolling page before anything comes back.

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/linkedin.com/get_connections`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/linkedin.com/get_connections
```

## Input

- `count` (integer, optional): How many connections to return, newest first. Default 100. LinkedIn loads 10 per step, so a large count on a large network takes long and counts against the account: ask for all of them only when you need them.

## Output

- `total` (integer, required): The connection count LinkedIn shows above the list.
- `complete` (boolean, required): True when connections holds every connection (total reached). False when count stopped the list first.
- `connections` (array, required): Newest first, as LinkedIn sorts them by default.

## Example output

Shape only: placeholder values generated from the output schema, not a real run.

```json
{
  "total": 3,
  "complete": true,
  "connections": [
    {
      "name": "Example",
      "headline": "…",
      "publicId": "abc123",
      "memberUrn": "abc123",
      "profileUrl": "https://example.com/item/123",
      "connectedOnText": "…"
    }
  ]
}
```

## FAQ

### What does "Get LinkedIn connections" do?

List the signed-in member's 1st-degree LinkedIn connections (My Network > Connections), newest first, up to count (default 100). Returns the total connection count LinkedIn shows, complete (true when the list reached its end), and each connection's name, headline, profile URL, public id, member URN and the connected-on date as shown. The list can end a little short of the total: LinkedIn counts some connections it does not list. LinkedIn loads 10 connections per step, so a large count takes long and counts against the account. When the list stops loading in the middle, the run fails and says where it stopped; it never returns part of the list as all of it.

### How do I automatically get LinkedIn connections on linkedin.com?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/get_connections, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/get_connections

### Is there a linkedin.com API to get LinkedIn connections?

You do not need one. "Get LinkedIn connections" drives the real linkedin.com pages in a browser, so it works whether or not linkedin.com offers an API for this.

### What information do I need to provide?

Optional: count.

### What does it return?

It returns total, complete, connections.

### Do I need to be logged in to linkedin.com?

Yes. It acts as you on linkedin.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the linkedin.com cookies saved by the Reduck extension.

### Does it change anything on linkedin.com, or only read data?

It only reads. It looks things up on linkedin.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/get_connections, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/get_connections

### Who maintains it?

It is part of Reduck's official curated catalogue.

### Why do I get fewer connections than the total LinkedIn shows?

Either your count capped the result, or the list stopped growing. The scroll loop ends once about 6 seconds pass without a new card, then returns what is loaded. On networks of several thousand, compare connections.length with total and run it again if the gap matters.

### Can I list another person's LinkedIn connections?

Only the signed-in account's own 1st-degree list comes back, never another member's. The page it reads is the Connections list under My Network, which belongs to the logged-in account.

### What format is the connection date in?

connectedOnText holds the Connected on line exactly as LinkedIn displays it, in your account's language. Nothing converts it to an ISO date, so the parsing happens on your side.

Source: https://reduck.ai/explore/scripts/reduck/linkedin.com/get_connections
