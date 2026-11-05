# List HubSpot deals

Automatically list HubSpot deals on app.hubspot.com. List the deals in a HubSpot account, newest first: name, amount, pipeline, stage, close date, owner, type, priority and dates, with the ids the deal scripts take. Optionally search by text and narrow to one pipeline, stage or owner. Pages with count and offset; an empty list means no deal matched. Finds the account and its region automatically; pass portalId when the login has several accounts.

- Site: app.hubspot.com
- Address: `reduck/app.hubspot.com/list_deals`
- Updated: 2026-11-04 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/app.hubspot.com/list_deals`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/app.hubspot.com/list_deals
```

## Input

- `count` (integer, optional)
- `query` (string, optional): Text to search deals for, e.g. part of a deal name.
- `stage` (string, optional): A stage id or name, to list only deals in it (within pipeline, or the default pipeline).
- `offset` (integer, optional): How many deals to skip: the nextOffset of the previous page.
- `ownerId` (string, optional): An owner id (as returned in ownerId), to list only that owner's deals.
- `pipeline` (string, optional): A pipeline id or name, to list only its deals.
- `portalId` (string, optional): The HubSpot account id, when the login has more than one.

## Output

- `deals` (array, required)
- `total` (integer, required)
- `hasMore` (boolean, required)
- `portalId` (string, required)
- `nextOffset` (integer | null, optional)
- `accountName` (string | null, optional)

## FAQ

### What does "List HubSpot deals" do?

List the deals in a HubSpot account, newest first: name, amount, pipeline, stage, close date, owner, type, priority and dates, with the ids the deal scripts take. Optionally search by text and narrow to one pipeline, stage or owner. Pages with count and offset; an empty list means no deal matched. Finds the account and its region automatically; pass portalId when the login has several accounts.

### How do I automatically list HubSpot deals on app.hubspot.com?

Ask an AI agent connected to Reduck to run reduck/app.hubspot.com/list_deals, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/app.hubspot.com/list_deals

### Is there a app.hubspot.com API to list HubSpot deals?

You do not need one. "List HubSpot deals" drives the real app.hubspot.com pages in a browser, so it works whether or not app.hubspot.com offers an API for this.

### What information do I need to provide?

Optional: count, query, stage, offset, ownerId, pipeline, portalId.

### What does it return?

It returns deals, total, hasMore, portalId, nextOffset, accountName.

### Do I need to be logged in to app.hubspot.com?

Yes. It acts as you on app.hubspot.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the app.hubspot.com cookies saved by the Reduck extension.

### Does it change anything on app.hubspot.com, or only read data?

It only reads. It looks things up on app.hubspot.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/app.hubspot.com/list_deals, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/app.hubspot.com/list_deals

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/app.hubspot.com/list_deals
