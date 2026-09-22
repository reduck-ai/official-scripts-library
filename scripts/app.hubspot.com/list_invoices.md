# List HubSpot invoices

Automatically list HubSpot invoices on app.hubspot.com. List the billing invoices on a HubSpot account, taken from Account & Billing → Transactions: each invoice's number, date, amount, status, and a link to its PDF. The PDF link is tied to the signed-in session, so it only opens while that session is still active. Sign in to HubSpot in the browser this runs against before using it — signed out, the script says so rather than returning an empty list. Pass portalId to target a specific portal when the account has more than one.

- Site: app.hubspot.com
- Address: `reduck/app.hubspot.com/list_invoices`
- Updated: 2026-08-07 (v5)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/app.hubspot.com/list_invoices`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/app.hubspot.com/list_invoices
```

## Input

- `portalId` (string, optional): HubSpot portal/hub id (e.g. 147691106). Omit to auto-detect from the logged-in session.

## Output

- `count` (number, required)
- `invoices` (array, required)
- `portalId` (string | null, required)

## FAQ

### What does "List HubSpot invoices" do?

List the billing invoices on a HubSpot account, taken from Account & Billing → Transactions: each invoice's number, date, amount, status, and a link to its PDF. The PDF link is tied to the signed-in session, so it only opens while that session is still active. Sign in to HubSpot in the browser this runs against before using it — signed out, the script says so rather than returning an empty list. Pass portalId to target a specific portal when the account has more than one.

### How do I automatically list HubSpot invoices on app.hubspot.com?

Ask an AI agent connected to Reduck to run reduck/app.hubspot.com/list_invoices, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/app.hubspot.com/list_invoices

### Is there a app.hubspot.com API to list HubSpot invoices?

You do not need one. "List HubSpot invoices" drives the real app.hubspot.com pages in a browser, so it works whether or not app.hubspot.com offers an API for this.

### What information do I need to provide?

Optional: portalId.

### What does it return?

It returns count, invoices, portalId.

### Do I need to be logged in to app.hubspot.com?

Yes. It acts as you on app.hubspot.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the app.hubspot.com cookies saved by the Reduck extension.

### Does it change anything on app.hubspot.com, or only read data?

It only reads. It looks things up on app.hubspot.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/app.hubspot.com/list_invoices, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/app.hubspot.com/list_invoices

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/app.hubspot.com/list_invoices
