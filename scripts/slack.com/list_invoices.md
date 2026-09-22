# List Slack invoices

Automatically list Slack invoices on slack.com. List Slack billing statements from the workspace's admin billing history. Returns workspace, total and invoices (date, statement, billId, amount, status, description, pdfUrl) — metadata only. Feed a row's pdfUrl (or billId) to slack.com/download_invoice to fetch that statement's PDF. Requires a workspace billing admin; defaults to the primary workspace, or pass workspaceDomain (e.g. acme.slack.com).

- Site: slack.com
- Address: `reduck/slack.com/list_invoices`
- Updated: 2026-08-21 (v7)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/slack.com/list_invoices`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/slack.com/list_invoices
```

## Input

- `workspaceDomain` (string, optional): Workspace host to target, e.g. acme.slack.com. Defaults to my.slack.com (primary workspace).

## Output

- `total` (integer, required)
- `invoices` (array, required)
- `workspace` (string, optional)

## FAQ

### What does "List Slack invoices" do?

List Slack billing statements from the workspace's admin billing history. Returns workspace, total and invoices (date, statement, billId, amount, status, description, pdfUrl) — metadata only. Feed a row's pdfUrl (or billId) to slack.com/download_invoice to fetch that statement's PDF. Requires a workspace billing admin; defaults to the primary workspace, or pass workspaceDomain (e.g. acme.slack.com).

### How do I automatically list Slack invoices on slack.com?

Ask an AI agent connected to Reduck to run reduck/slack.com/list_invoices, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/slack.com/list_invoices

### Is there a slack.com API to list Slack invoices?

You do not need one. "List Slack invoices" drives the real slack.com pages in a browser, so it works whether or not slack.com offers an API for this.

### What information do I need to provide?

Optional: workspaceDomain.

### What does it return?

It returns total, invoices, workspace.

### Do I need to be logged in to slack.com?

Yes. It acts as you on slack.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the slack.com cookies saved by the Reduck extension.

### Does it change anything on slack.com, or only read data?

It only reads. It looks things up on slack.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/slack.com/list_invoices, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/slack.com/list_invoices

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/slack.com/list_invoices
