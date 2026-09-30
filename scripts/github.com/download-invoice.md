# Download GitHub invoice/receipt

Automatically download GitHub invoice/receipt on github.com. Download a single GitHub billing document (receipt or formal invoice) as PDF, by url/filename from github.com/list-invoices. Returns the PDF bytes as base64 plus the filename.

- Site: github.com
- Address: `reduck/github.com/download-invoice`
- Updated: 2026-09-29 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/github.com/download-invoice`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/github.com/download-invoice
```

## Input

- `url` (string, required): url from the receipt/invoice object returned by github.com/list-invoices.
- `filename` (string, required): filename from the same object.

## Output

- `filename` (string, required)
- `contentBase64` (string, required)

## FAQ

### What does "Download GitHub invoice/receipt" do?

Download a single GitHub billing document (receipt or formal invoice) as PDF, by url/filename from github.com/list-invoices. Returns the PDF bytes as base64 plus the filename.

### How do I automatically download GitHub invoice/receipt on github.com?

Ask an AI agent connected to Reduck to run reduck/github.com/download-invoice, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/github.com/download-invoice

### Is there a github.com API to download GitHub invoice/receipt?

You do not need one. "Download GitHub invoice/receipt" drives the real github.com pages in a browser, so it works whether or not github.com offers an API for this.

### What information do I need to provide?

Required: url, filename.

### What does it return?

It returns filename, contentBase64.

### Do I need to be logged in to github.com?

Yes. It acts as you on github.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the github.com cookies saved by the Reduck extension.

### Does it change anything on github.com, or only read data?

It only reads. It looks things up on github.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/github.com/download-invoice, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/github.com/download-invoice

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/github.com/download-invoice
