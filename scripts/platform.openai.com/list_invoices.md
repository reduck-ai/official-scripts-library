# List OpenAI platform invoices

Automatically list OpenAI platform invoices on platform.openai.com. List the invoices of an OpenAI API platform billing account (API usage and credits; for the ChatGPT subscription use chatgpt.com/list_invoices). Returns id, number, total (in cents), amount paid, currency, status, creation time, hosted invoice link and PDF link. Covers the past 12 months, as the billing page does. An account in several organizations picks the first one offered, or the one named exactly by organization; an unknown name fails and lists the organizations offered.

- Site: platform.openai.com
- Address: `reduck/platform.openai.com/list_invoices`
- Updated: 2026-10-19 (v5)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/platform.openai.com/list_invoices`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/platform.openai.com/list_invoices
```

## Input

- `organization` (string, optional): Which API organization to use if OpenAI asks you to choose one, by its exact name as shown. When no organization has that name the run stops and lists them. Defaults to the first one offered.

## Output

- `invoices` (array, required)

## FAQ

### What does "List OpenAI platform invoices" do?

List the invoices of an OpenAI API platform billing account (API usage and credits; for the ChatGPT subscription use chatgpt.com/list_invoices). Returns id, number, total (in cents), amount paid, currency, status, creation time, hosted invoice link and PDF link. Covers the past 12 months, as the billing page does. An account in several organizations picks the first one offered, or the one named exactly by organization; an unknown name fails and lists the organizations offered.

### How do I automatically list OpenAI platform invoices on platform.openai.com?

Ask an AI agent connected to Reduck to run reduck/platform.openai.com/list_invoices, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/platform.openai.com/list_invoices

### Is there a platform.openai.com API to list OpenAI platform invoices?

You do not need one. "List OpenAI platform invoices" drives the real platform.openai.com pages in a browser, so it works whether or not platform.openai.com offers an API for this.

### What information do I need to provide?

Optional: organization.

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
