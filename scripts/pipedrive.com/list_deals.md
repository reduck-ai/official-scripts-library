# List Pipedrive deals

Automatically list Pipedrive deals on pipedrive.com. List deals from Pipedrive's Deals list view, reading whatever columns the current view shows (title, value, organization, contact person, expected close date, next activity date, owner). Returns each deal's id and its visible column values.

- Site: pipedrive.com
- Address: `reduck/pipedrive.com/list_deals`
- Updated: 2026-09-04 (v6)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/pipedrive.com/list_deals`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/pipedrive.com/list_deals
```

## Input

- `workspace` (string, required): Pipedrive workspace subdomain, e.g. "acme" (the segment right before .pipedrive.com)

## Output

- `deals` (array, required)

## FAQ

### What does "List Pipedrive deals" do?

List deals from Pipedrive's Deals list view, reading whatever columns the current view shows (title, value, organization, contact person, expected close date, next activity date, owner). Returns each deal's id and its visible column values.

### How do I automatically list Pipedrive deals on pipedrive.com?

Ask an AI agent connected to Reduck to run reduck/pipedrive.com/list_deals, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/pipedrive.com/list_deals

### Is there a pipedrive.com API to list Pipedrive deals?

You do not need one. "List Pipedrive deals" drives the real pipedrive.com pages in a browser, so it works whether or not pipedrive.com offers an API for this.

### What information do I need to provide?

Required: workspace.

### What does it return?

It returns deals.

### Do I need to be logged in to pipedrive.com?

Yes. It acts as you on pipedrive.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the pipedrive.com cookies saved by the Reduck extension.

### Does it change anything on pipedrive.com, or only read data?

It only reads. It looks things up on pipedrive.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/pipedrive.com/list_deals, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/pipedrive.com/list_deals

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/pipedrive.com/list_deals
