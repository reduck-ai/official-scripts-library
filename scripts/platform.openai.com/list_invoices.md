# List OpenAI API invoices

Automatically list OpenAI API invoices on platform.openai.com. List invoices on the OpenAI API platform billing account (platform.openai.com, api usage/credits — NOT the ChatGPT subscription). Returns id, number, total (cents), currency, status, created_ts, hosted_invoice_url, pdf_url. Covers the past 12 months, as the dashboard does.

- Site: platform.openai.com
- Address: `reduck/platform.openai.com/list_invoices`
- Updated: 2026-07-31 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/platform.openai.com/list_invoices`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/platform.openai.com/list_invoices
```

## Input

It takes no input.

## Output

- `invoices` (array, required)

## FAQ

### What does "List OpenAI API invoices" do?

List invoices on the OpenAI API platform billing account (platform.openai.com, api usage/credits — NOT the ChatGPT subscription). Returns id, number, total (cents), currency, status, created_ts, hosted_invoice_url, pdf_url. Covers the past 12 months, as the dashboard does.

### How do I automatically list OpenAI API invoices on platform.openai.com?

Ask an AI agent connected to Reduck to run reduck/platform.openai.com/list_invoices, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/platform.openai.com/list_invoices

### Is there a platform.openai.com API to list OpenAI API invoices?

You do not need one. "List OpenAI API invoices" drives the real platform.openai.com pages in a browser, so it works whether or not platform.openai.com offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns invoices.

### Do I need to be logged in to platform.openai.com?

Yes. It acts as you on platform.openai.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the platform.openai.com cookies saved by the Reduck extension.

### Does it change anything on platform.openai.com, or only read data?

Unknown: its author has not declared whether it changes anything on platform.openai.com, so treat it as if it could.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/platform.openai.com/list_invoices, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/platform.openai.com/list_invoices

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/platform.openai.com/list_invoices
