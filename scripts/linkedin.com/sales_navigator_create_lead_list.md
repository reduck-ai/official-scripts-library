# Sales Navigator – Create lead list

Automatically create lead list on linkedin.com. Creates a new manual LinkedIn Sales Navigator lead list. Takes a name and optional description, returns the new listId (the join key that feeds save_lead_to_list and get_lead_list). This changes your account and needs a Sales Navigator seat.

- Site: linkedin.com
- Address: `reduck/linkedin.com/sales_navigator_create_lead_list`
- Updated: 2026-08-26 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/linkedin.com/sales_navigator_create_lead_list`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/linkedin.com/sales_navigator_create_lead_list
```

## Input

- `name` (string, required): Name for the new lead list.
- `description` (string, optional): Optional description for the list.

## Output

- `name` (string, required)
- `listId` (string, required): New Sales Navigator lead list id — the join key for save_lead_to_list and get_lead_list.
- `listUrl` (string, required)
- `createdAt` (integer | null, optional): Epoch ms.
- `description` (string | null, optional)
- `nameCollision` (boolean, optional): True when the account already had another LEAD list with this exact name (LinkedIn allows duplicates).

## FAQ

### What does "Sales Navigator – Create lead list" do?

Creates a new manual LinkedIn Sales Navigator lead list. Takes a name and optional description, returns the new listId (the join key that feeds save_lead_to_list and get_lead_list). This changes your account and needs a Sales Navigator seat.

### How do I automatically create lead list on linkedin.com?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/sales_navigator_create_lead_list, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/sales_navigator_create_lead_list

### Is there a linkedin.com API to create lead list?

You do not need one. "Sales Navigator – Create lead list" drives the real linkedin.com pages in a browser, so it works whether or not linkedin.com offers an API for this.

### What information do I need to provide?

Required: name. Optional: description.

### What does it return?

It returns name, listId, listUrl, createdAt, description, nameCollision.

### Do I need to be logged in to linkedin.com?

Yes. It acts as you on linkedin.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the linkedin.com cookies saved by the Reduck extension.

### Does it change anything on linkedin.com, or only read data?

It makes changes on linkedin.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/sales_navigator_create_lead_list, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/sales_navigator_create_lead_list

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/linkedin.com/sales_navigator_create_lead_list
