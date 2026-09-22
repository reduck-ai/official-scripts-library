# Download a Slack invoice PDF

Automatically download a Slack invoice PDF on slack.com. Download one Slack billing statement, given the pdfUrl or billId that slack.com/list_invoices returns. Returns the real filename plus the file bytes inline as base64, so decode and write it yourself — nothing is left on disk. Requires being a workspace billing admin.

- Site: slack.com
- Address: `reduck/slack.com/download_invoice`
- Updated: 2026-08-26 (v1)
- Author: Reduck AI (reduck)

## About

Developers looking for a Slack API to download a Slack invoice PDF usually find there is none they can use: Slack's API has no billing or invoice endpoint. This script fills that gap. It works like an API endpoint — one call with typed arguments, a JSON response — but runs through a real browser, yours or a hosted one, so it needs no Slack developer account, API key or app review.

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/slack.com/download_invoice`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/slack.com/download_invoice
```

## Input

- `billId` (string, optional): A bill ID from slack.com/list_invoices, used only when pdfUrl is not given. Combined with workspaceDomain to build the URL.
- `pdfUrl` (string, optional): The statement's download URL as returned by slack.com/list_invoices (https://<workspace>.slack.com/admin/billing/<billId>/pdf). Preferred over billId.
- `workspaceDomain` (string, optional): Workspace host to target when using billId, e.g. acme.slack.com. Defaults to my.slack.com (primary workspace). Ignored when pdfUrl is given.

## Output

- `filename` (string, required): The real suggested filename, taken from the file's Content-Disposition (e.g. Slack-Statement-SBIE-10873175.pdf). Falls back to Slack-<billId>.<ext> if Slack sends no Content-Disposition.
- `pdf_base64` (string, required): The file bytes, base64-encoded. Decode and write it yourself — the script is sandboxed and cannot write to disk.
- `size_bytes` (integer, optional): Byte length of the decoded file.
- `content_type` (string | null, optional): The file's own MIME type. Normally application/pdf; Slack answers application/zip for a bundled statement, in which case pdf_base64 holds zip bytes and filename ends in .zip.

## FAQ

### What does "Download a Slack invoice PDF" do?

Download one Slack billing statement, given the pdfUrl or billId that slack.com/list_invoices returns. Returns the real filename plus the file bytes inline as base64, so decode and write it yourself — nothing is left on disk. Requires being a workspace billing admin.

### How do I automatically download a Slack invoice PDF on slack.com?

Ask an AI agent connected to Reduck to run reduck/slack.com/download_invoice, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/slack.com/download_invoice

### Is there a slack.com API to download a Slack invoice PDF?

You do not need one. "Download a Slack invoice PDF" drives the real slack.com pages in a browser, so it works whether or not slack.com offers an API for this.

### What information do I need to provide?

Optional: billId, pdfUrl, workspaceDomain.

### What does it return?

It returns filename, pdf_base64, size_bytes, content_type.

### Do I need to be logged in to slack.com?

Yes. It acts as you on slack.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the slack.com cookies saved by the Reduck extension.

### Does it change anything on slack.com, or only read data?

It only reads. It looks things up on slack.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/slack.com/download_invoice, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/slack.com/download_invoice

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/slack.com/download_invoice
