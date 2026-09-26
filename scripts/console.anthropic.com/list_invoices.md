# List Anthropic Console invoices

Automatically list Anthropic Console invoices on console.anthropic.com. List the billing invoices on the signed-in Anthropic Console (platform.claude.com) organization: date, type, invoice number, status, amount and each invoice's Stripe-hosted page, plus the organization id and name. Reads the whole invoice history, following pagination, and works whatever language the Console is in. An organization with no invoices returns an empty list; signed out, it stops with a clear error rather than returning nothing. The Stripe links are re-signed on every load, so use them rather than store them.

- Site: console.anthropic.com
- Address: `reduck/console.anthropic.com/list_invoices`
- Updated: 2026-09-25 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/console.anthropic.com/list_invoices`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/console.anthropic.com/list_invoices
```

## Input

It takes no input.

## Output

- `count` (number, required): 0 is a real answer: the organization has no invoice history.
- `invoices` (array, required)
- `organizationId` (string, required)
- `pages` (number, optional): How many pages of the history were read.
- `organizationName` (string | null, optional)

## FAQ

### What does "List Anthropic Console invoices" do?

List the billing invoices on the signed-in Anthropic Console (platform.claude.com) organization: date, type, invoice number, status, amount and each invoice's Stripe-hosted page, plus the organization id and name. Reads the whole invoice history, following pagination, and works whatever language the Console is in. An organization with no invoices returns an empty list; signed out, it stops with a clear error rather than returning nothing. The Stripe links are re-signed on every load, so use them rather than store them.

### How do I automatically list Anthropic Console invoices on console.anthropic.com?

Ask an AI agent connected to Reduck to run reduck/console.anthropic.com/list_invoices, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/console.anthropic.com/list_invoices

### Is there a console.anthropic.com API to list Anthropic Console invoices?

You do not need one. "List Anthropic Console invoices" drives the real console.anthropic.com pages in a browser, so it works whether or not console.anthropic.com offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns count, pages, invoices, organizationId, organizationName.

### Do I need to be logged in to console.anthropic.com?

Yes. It acts as you on console.anthropic.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the console.anthropic.com cookies saved by the Reduck extension.

### Does it change anything on console.anthropic.com, or only read data?

It only reads. It looks things up on console.anthropic.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/console.anthropic.com/list_invoices, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/console.anthropic.com/list_invoices

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/console.anthropic.com/list_invoices
