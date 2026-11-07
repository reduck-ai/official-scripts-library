# Download ClickUp invoice

Automatically download ClickUp invoice on app.clickup.com. Download one ClickUp workspace invoice PDF by its invoice number. Returns the saved file (path or url) and its filename.

- Site: app.clickup.com
- Address: `reduck/app.clickup.com/download_invoice`
- Updated: 2026-11-06 (v4)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/app.clickup.com/download_invoice`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/app.clickup.com/download_invoice
```

## Input

- `number` (string, required): Invoice number from app.clickup.com/list_invoices.
- `workspaceId` (string, optional): Numeric ClickUp workspace/team id. Omit to auto-detect the current session's workspace.

## Output

- `filename` (string, required): Saved file name; can end in " (2)".
- `url` (string, optional): Where to fetch the file (managed browser).
- `path` (string, optional): Where the file was saved on the machine running the browser (user's Chrome).

## FAQ

### What does "Download ClickUp invoice" do?

Download one ClickUp workspace invoice PDF by its invoice number. Returns the saved file (path or url) and its filename.

### How do I automatically download ClickUp invoice on app.clickup.com?

Ask an AI agent connected to Reduck to run reduck/app.clickup.com/download_invoice, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/app.clickup.com/download_invoice

### Is there a app.clickup.com API to download ClickUp invoice?

You do not need one. "Download ClickUp invoice" drives the real app.clickup.com pages in a browser, so it works whether or not app.clickup.com offers an API for this.

### What information do I need to provide?

Required: number. Optional: workspaceId.

### What does it return?

It returns url, path, filename.

### Do I need to be logged in to app.clickup.com?

Yes. It acts as you on app.clickup.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the app.clickup.com cookies saved by the Reduck extension.

### Does it change anything on app.clickup.com, or only read data?

It only reads. It looks things up on app.clickup.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/app.clickup.com/download_invoice, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/app.clickup.com/download_invoice

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/app.clickup.com/download_invoice
