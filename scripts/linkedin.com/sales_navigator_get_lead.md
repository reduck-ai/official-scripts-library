# Sales Navigator: get lead

Automatically get lead on linkedin.com. Fetch a full LinkedIn Sales Navigator lead profile by its lead id (from search_people). Requires a Sales Navigator seat; contactInfo is empty unless the lead is unlocked for the seat. Returns fullName, headline, summary, degree, location, classic LinkedIn profile URL, full position history (title, company, companyUrn, description, dates), saved-list status, and contact info when unlocked.

- Site: linkedin.com
- Address: `reduck/linkedin.com/sales_navigator_get_lead`
- Updated: 2026-09-03 (v5)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/linkedin.com/sales_navigator_get_lead`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/linkedin.com/sales_navigator_get_lead
```

## Input

- `leadId` (string, required): Sales Navigator lead id from sales_navigator_search_people. The raw value including any search-context suffix (e.g. "ACwAAB...,NAME_SEARCH,Sgkj") is accepted — it is normalized to the bare profile id.

## Output

- `leadId` (string, required)
- `fullName` (string, required)
- `degree` (integer | null, optional)
- `summary` (string | null, optional)
- `headline` (string | null, optional)
- `lastName` (string | null, optional)
- `location` (string | null, optional)
- `unlocked` (boolean, optional): Whether the lead's contact info is unlocked for this seat.
- `firstName` (string | null, optional)
- `listCount` (integer | null, optional)
- `memberUrn` (string | null, optional): urn:li:member:N — classic LinkedIn member id.
- `positions` (array, optional)
- `savedLead` (boolean, optional)
- `contactInfo` (object, optional): Emails/phones/websites when unlocked; {} otherwise.
- `currentPosition` (object | null, optional)
- `flagshipProfileUrl` (string | null, optional): Classic linkedin.com/in/ profile URL.

## FAQ

### What does "Sales Navigator: get lead" do?

Fetch a full LinkedIn Sales Navigator lead profile by its lead id (from search_people). Requires a Sales Navigator seat; contactInfo is empty unless the lead is unlocked for the seat. Returns fullName, headline, summary, degree, location, classic LinkedIn profile URL, full position history (title, company, companyUrn, description, dates), saved-list status, and contact info when unlocked.

### How do I automatically get lead on linkedin.com?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/sales_navigator_get_lead, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/sales_navigator_get_lead

### Is there a linkedin.com API to get lead?

You do not need one. "Sales Navigator: get lead" drives the real linkedin.com pages in a browser, so it works whether or not linkedin.com offers an API for this.

### What information do I need to provide?

Required: leadId.

### What does it return?

It returns degree, leadId, summary, fullName, headline, lastName, location, unlocked, firstName, listCount, memberUrn, positions, savedLead, contactInfo, currentPosition, flagshipProfileUrl.

### Do I need to be logged in to linkedin.com?

Yes. It acts as you on linkedin.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the linkedin.com cookies saved by the Reduck extension.

### Does it change anything on linkedin.com, or only read data?

Unknown: its author has not declared whether it changes anything on linkedin.com, so treat it as if it could.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/sales_navigator_get_lead, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/sales_navigator_get_lead

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/linkedin.com/sales_navigator_get_lead
