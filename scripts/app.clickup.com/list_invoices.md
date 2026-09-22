# ClickUp — list invoices

Automatically list invoices on app.clickup.com. List a ClickUp workspace's billing invoices (date, number, amount); optional download saves each PDF to the browser's Downloads folder.

- Site: app.clickup.com
- Address: `reduck/app.clickup.com/list_invoices`
- Updated: 2026-08-21 (v6)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/app.clickup.com/list_invoices`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/app.clickup.com/list_invoices
```

## Input

- `workspaceId` (string, optional): Numeric ClickUp workspace/team id (e.g. "90152247542"). Omit to auto-detect the current session's workspace via /settings/billing-details redirect.

## Output

- `invoices` (array, required)
- `workspaceId` (string, required)

## FAQ

### What does "ClickUp — list invoices" do?

List a ClickUp workspace's billing invoices (date, number, amount); optional download saves each PDF to the browser's Downloads folder.

### How do I automatically list invoices on app.clickup.com?

Ask an AI agent connected to Reduck to run reduck/app.clickup.com/list_invoices, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/app.clickup.com/list_invoices

### Is there a app.clickup.com API to list invoices?

You do not need one. "ClickUp — list invoices" drives the real app.clickup.com pages in a browser, so it works whether or not app.clickup.com offers an API for this.

### What information do I need to provide?

Optional: workspaceId.

### What does it return?

It returns invoices, workspaceId.

### Do I need to be logged in to app.clickup.com?

Yes. It acts as you on app.clickup.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the app.clickup.com cookies saved by the Reduck extension.

### Does it change anything on app.clickup.com, or only read data?

It only reads. It looks things up on app.clickup.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/app.clickup.com/list_invoices, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/app.clickup.com/list_invoices

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/app.clickup.com/list_invoices
