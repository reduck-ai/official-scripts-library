# Sales Navigator — list account lists

Automatically list account lists on linkedin.com. List the viewer's Sales Navigator account lists (the saved-companies lists). Returns each list's id (the join key for saving accounts), name, description, source (manual, system, CRM and so on), role, entityCount and last-modified/-viewed timestamps, most-recently-modified first. Returns the first page (25) plus the exact total so truncation is visible; needs a Sales Navigator seat.

- Site: linkedin.com
- Address: `reduck/linkedin.com/sales_navigator_list_account_lists`
- Updated: 2026-09-03 (v4)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/linkedin.com/sales_navigator_list_account_lists`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/linkedin.com/sales_navigator_list_account_lists
```

## Input

It takes no input.

## Output

- `count` (integer, required)
- `lists` (array, required)
- `total` (integer, required): Exact number of ACCOUNT lists the viewer owns (paging.total). If greater than count, more exist beyond this first page.

## FAQ

### What does "Sales Navigator — list account lists" do?

List the viewer's Sales Navigator account lists (the saved-companies lists). Returns each list's id (the join key for saving accounts), name, description, source (manual, system, CRM and so on), role, entityCount and last-modified/-viewed timestamps, most-recently-modified first. Returns the first page (25) plus the exact total so truncation is visible; needs a Sales Navigator seat.

### How do I automatically list account lists on linkedin.com?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/sales_navigator_list_account_lists, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/sales_navigator_list_account_lists

### Is there a linkedin.com API to list account lists?

You do not need one. "Sales Navigator — list account lists" drives the real linkedin.com pages in a browser, so it works whether or not linkedin.com offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns count, lists, total.

### Do I need to be logged in to linkedin.com?

Yes. It acts as you on linkedin.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the linkedin.com cookies saved by the Reduck extension.

### Does it change anything on linkedin.com, or only read data?

It only reads. It looks things up on linkedin.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/sales_navigator_list_account_lists, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/sales_navigator_list_account_lists

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/linkedin.com/sales_navigator_list_account_lists
