# Sales Navigator – Get lead list contents

Automatically get lead list contents on linkedin.com. List the leads saved inside a LinkedIn Sales Navigator lead list, by list id (from list_lead_lists), paginated via start/count (default 25, newest-added first). Returns total and leads (salesProfileUrn - feeds save_lead_to_list and get_lead - plus salesLeadUrl, name, degree, geoRegion, current title/company, listCount, dateAddedToListAt, crmStatus). Needs a Sales Navigator seat.

- Site: linkedin.com
- Address: `reduck/linkedin.com/sales_navigator_get_lead_list`
- Updated: 2026-09-03 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/linkedin.com/sales_navigator_get_lead_list`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/linkedin.com/sales_navigator_get_lead_list
```

## Input

- `listId` (string, required): Lead list id (numeric string) from list_lead_lists.
- `count` (integer, optional): Leads per page. Default 25. Order is dateAdded DESC and stable, so start is safe to fan out.
- `start` (integer, optional): 0-based offset for pagination. Default 0.

## Output

- `leads` (array, required)
- `listId` (string, required)
- `count` (integer, optional)
- `start` (integer, optional)
- `total` (integer | null, optional): Total leads in the list.

## FAQ

### What does "Sales Navigator – Get lead list contents" do?

List the leads saved inside a LinkedIn Sales Navigator lead list, by list id (from list_lead_lists), paginated via start/count (default 25, newest-added first). Returns total and leads (salesProfileUrn - feeds save_lead_to_list and get_lead - plus salesLeadUrl, name, degree, geoRegion, current title/company, listCount, dateAddedToListAt, crmStatus). Needs a Sales Navigator seat.

### How do I automatically get lead list contents on linkedin.com?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/sales_navigator_get_lead_list, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/sales_navigator_get_lead_list

### Is there a linkedin.com API to get lead list contents?

You do not need one. "Sales Navigator – Get lead list contents" drives the real linkedin.com pages in a browser, so it works whether or not linkedin.com offers an API for this.

### What information do I need to provide?

Required: listId. Optional: count, start.

### What does it return?

It returns count, leads, start, total, listId.

### Do I need to be logged in to linkedin.com?

Yes. It acts as you on linkedin.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the linkedin.com cookies saved by the Reduck extension.

### Does it change anything on linkedin.com, or only read data?

Unknown: its author has not declared whether it changes anything on linkedin.com, so treat it as if it could.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/sales_navigator_get_lead_list, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/sales_navigator_get_lead_list

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/linkedin.com/sales_navigator_get_lead_list
