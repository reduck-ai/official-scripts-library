# Sales Navigator – Export lead list (all pages)

Automatically export lead list (all pages) on linkedin.com. Export every lead in a LinkedIn Sales Navigator lead list, by list id (from list_lead_lists), looping all pages instead of stopping at the first 25 like get_lead_list. Returns total, the full leads array (salesProfileUrn, salesLeadUrl, name, degree, geoRegion, current title/company, listCount, dateAddedToListAt, crmStatus) and a `complete` flag so a truncated export can never be mistaken for a whole one. Needs a Sales Navigator seat.

- Site: linkedin.com
- Address: `reduck/linkedin.com/sales_navigator_export_lead_list`
- Updated: 2026-09-03 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/linkedin.com/sales_navigator_export_lead_list`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/linkedin.com/sales_navigator_export_lead_list
```

## Input

- `listId` (string, required): Lead list id (numeric string) from list_lead_lists.
- `maxLeads` (integer, optional): Safety cap on how many leads to pull. Default 5000. If the list is larger, `complete` comes back false.
- `pageSize` (integer, optional): Leads per request. Default 25 (what the page itself uses).

## Output

- `count` (integer, required): Leads actually returned.
- `leads` (array, required)
- `total` (integer | null, required): Total leads the list reports.
- `listId` (string, required)
- `complete` (boolean, required): True only when count reached total. False means the export was cut short (cap hit or paging stalled) — treat the data as partial.
- `pages` (integer, optional): Number of requests made.
- `truncatedReason` (string | null, optional): Why the export stopped early, when complete is false.

## FAQ

### What does "Sales Navigator – Export lead list (all pages)" do?

Export every lead in a LinkedIn Sales Navigator lead list, by list id (from list_lead_lists), looping all pages instead of stopping at the first 25 like get_lead_list. Returns total, the full leads array (salesProfileUrn, salesLeadUrl, name, degree, geoRegion, current title/company, listCount, dateAddedToListAt, crmStatus) and a `complete` flag so a truncated export can never be mistaken for a whole one. Needs a Sales Navigator seat.

### How do I automatically export lead list (all pages) on linkedin.com?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/sales_navigator_export_lead_list, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/sales_navigator_export_lead_list

### Is there a linkedin.com API to export lead list (all pages)?

You do not need one. "Sales Navigator – Export lead list (all pages)" drives the real linkedin.com pages in a browser, so it works whether or not linkedin.com offers an API for this.

### What information do I need to provide?

Required: listId. Optional: maxLeads, pageSize.

### What does it return?

It returns count, leads, pages, total, listId, complete, truncatedReason.

### Do I need to be logged in to linkedin.com?

Yes. It acts as you on linkedin.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the linkedin.com cookies saved by the Reduck extension.

### Does it change anything on linkedin.com, or only read data?

It only reads. It looks things up on linkedin.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/sales_navigator_export_lead_list, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/sales_navigator_export_lead_list

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/linkedin.com/sales_navigator_export_lead_list
