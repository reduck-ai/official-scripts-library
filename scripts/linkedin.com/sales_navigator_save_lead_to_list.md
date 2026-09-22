# Sales Navigator – Save lead(s) to list

Automatically save lead(s) to list on linkedin.com. Saves one or more LinkedIn Sales Navigator leads into one or more manual lead lists. Takes salesProfile urns (from search_people / get_lead_list / sales_navigator_get_lead) and list ids (from list_lead_lists), and returns a per-(lead, list) result that reports when the lead was already in that list rather than saving it again. Leads can only be saved to manual lists you own (not system or auto lists); this changes your account and needs a Sales Navigator seat.

- Site: linkedin.com
- Address: `reduck/linkedin.com/sales_navigator_save_lead_to_list`
- Updated: 2026-08-26 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/linkedin.com/sales_navigator_save_lead_to_list`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/linkedin.com/sales_navigator_save_lead_to_list
```

## Input

- `listIds` (array, required): Manual lead list ids (numeric strings) from list_lead_lists. Each lead is saved into every list.
- `leadUrns` (array, required): salesProfile urns, e.g. 'urn:li:fs_salesProfile:(ACwAA...,NAME_SEARCH,xxxx)', from search_people / get_lead_list / sales_navigator_get_lead.

## Output

- `results` (array, required): One entry per (lead, list) action.
- `requested` (object, required)

## FAQ

### What does "Sales Navigator – Save lead(s) to list" do?

Saves one or more LinkedIn Sales Navigator leads into one or more manual lead lists. Takes salesProfile urns (from search_people / get_lead_list / sales_navigator_get_lead) and list ids (from list_lead_lists), and returns a per-(lead, list) result that reports when the lead was already in that list rather than saving it again. Leads can only be saved to manual lists you own (not system or auto lists); this changes your account and needs a Sales Navigator seat.

### How do I automatically save lead(s) to list on linkedin.com?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/sales_navigator_save_lead_to_list, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/sales_navigator_save_lead_to_list

### Is there a linkedin.com API to save lead(s) to list?

You do not need one. "Sales Navigator – Save lead(s) to list" drives the real linkedin.com pages in a browser, so it works whether or not linkedin.com offers an API for this.

### What information do I need to provide?

Required: leadUrns, listIds.

### What does it return?

It returns results, requested.

### Do I need to be logged in to linkedin.com?

Yes. It acts as you on linkedin.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the linkedin.com cookies saved by the Reduck extension.

### Does it change anything on linkedin.com, or only read data?

It makes changes on linkedin.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/sales_navigator_save_lead_to_list, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/sales_navigator_save_lead_to_list

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/linkedin.com/sales_navigator_save_lead_to_list
