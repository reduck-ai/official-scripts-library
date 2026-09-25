# Search HubSpot contacts

Automatically search HubSpot contacts on app.hubspot.com. Search the contacts in a HubSpot account and return the matching rows with name, email, phone, owner, company and dates. Finds the right account and region automatically, and reports a search that matches nothing as an empty result.

- Site: app.hubspot.com
- Address: `reduck/app.hubspot.com/search_contacts`
- Updated: 2026-09-24 (v5)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/app.hubspot.com/search_contacts`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/app.hubspot.com/search_contacts
```

## Input

- `query` (string, required): Text to search contacts for — a name, an email, or part of either. Pass an empty string to list without filtering.
- `portalId` (string, optional): The HubSpot account id to read, when the login has more than one. Omit it to use the default account, or the only one.

## Output

- `query` (string, required)
- `contacts` (array, required)
- `portalId` (string, required): The HubSpot account the contacts were read from.
- `url` (string, optional)
- `columns` (array, optional): The contact table's column headings, in the account's own interface language. A named field below is filled only where its heading appears here.
- `matched` (boolean, optional): Whether the search returned any contacts at all. False means HubSpot reported the search as empty, which is an answer rather than a failure.
- `accountName` (string | null, optional)
- `contactCount` (number, optional)

## FAQ

### What does "Search HubSpot contacts" do?

Search the contacts in a HubSpot account and return the matching rows with name, email, phone, owner, company and dates. Finds the right account and region automatically, and reports a search that matches nothing as an empty result.

### How do I automatically search HubSpot contacts on app.hubspot.com?

Ask an AI agent connected to Reduck to run reduck/app.hubspot.com/search_contacts, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/app.hubspot.com/search_contacts

### Is there a app.hubspot.com API to search HubSpot contacts?

You do not need one. "Search HubSpot contacts" drives the real app.hubspot.com pages in a browser, so it works whether or not app.hubspot.com offers an API for this.

### What information do I need to provide?

Required: query. Optional: portalId.

### What does it return?

It returns url, query, columns, matched, contacts, portalId, accountName, contactCount.

### Do I need to be logged in to app.hubspot.com?

Yes. It acts as you on app.hubspot.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the app.hubspot.com cookies saved by the Reduck extension.

### Does it change anything on app.hubspot.com, or only read data?

It only reads. It looks things up on app.hubspot.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/app.hubspot.com/search_contacts, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/app.hubspot.com/search_contacts

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/app.hubspot.com/search_contacts
