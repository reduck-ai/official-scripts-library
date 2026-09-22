# List GitHub invoices

Automatically list GitHub invoices on github.com. List all GitHub billing invoices from the payment history. Returns date, amount, method, status, shortId, chargeId, pdfUrl, receiptUrl.

- Site: github.com
- Address: `reduck/github.com/list-invoices`
- Updated: 2026-09-08 (v10)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/github.com/list-invoices`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/github.com/list-invoices
```

## Input

- `enterprise` (string, optional): Enterprise slug (e.g. "my-enterprise") for an Enterprise account whose billing rolls up to the enterprise. Omit for personal-account billing. The formal invoice document is not supported for enterprise billing and comes back null.

## FAQ

### What does "List GitHub invoices" do?

List all GitHub billing invoices from the payment history. Returns date, amount, method, status, shortId, chargeId, pdfUrl, receiptUrl.

### How do I automatically list GitHub invoices on github.com?

Ask an AI agent connected to Reduck to run reduck/github.com/list-invoices, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/github.com/list-invoices

### Is there a github.com API to list GitHub invoices?

You do not need one. "List GitHub invoices" drives the real github.com pages in a browser, so it works whether or not github.com offers an API for this.

### What information do I need to provide?

Optional: enterprise.

### Do I need to be logged in to github.com?

Yes. It acts as you on github.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the github.com cookies saved by the Reduck extension.

### Does it change anything on github.com, or only read data?

It only reads. It looks things up on github.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/github.com/list-invoices, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/github.com/list-invoices

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/github.com/list-invoices
