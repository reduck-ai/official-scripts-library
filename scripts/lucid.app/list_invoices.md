# List Lucid (Lucidchart) invoices

Automatically list Lucid (Lucidchart) invoices on lucid.app. List Lucid (Lucidchart/Lucidspark) billing invoices, returning total plus each invoice's date, number, description and amount — metadata only. Feed a row's number to lucid.app/download_invoice to fetch that invoice's PDF. Works whatever language the account is set to. An account with no invoices returns an empty list, and a billing page that never finishes loading is reported as an error rather than passed off as an empty one.

- Site: lucid.app
- Address: `reduck/lucid.app/list_invoices`
- Updated: 2026-08-21 (v7)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/lucid.app/list_invoices`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/lucid.app/list_invoices
```

## Input

It takes no input.

## Output

- `total` (integer, required)
- `invoices` (array, required)

## FAQ

### What does "List Lucid (Lucidchart) invoices" do?

List Lucid (Lucidchart/Lucidspark) billing invoices, returning total plus each invoice's date, number, description and amount — metadata only. Feed a row's number to lucid.app/download_invoice to fetch that invoice's PDF. Works whatever language the account is set to. An account with no invoices returns an empty list, and a billing page that never finishes loading is reported as an error rather than passed off as an empty one.

### How do I automatically list Lucid (Lucidchart) invoices on lucid.app?

Ask an AI agent connected to Reduck to run reduck/lucid.app/list_invoices, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/lucid.app/list_invoices

### Is there a lucid.app API to list Lucid (Lucidchart) invoices?

You do not need one. "List Lucid (Lucidchart) invoices" drives the real lucid.app pages in a browser, so it works whether or not lucid.app offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns total, invoices.

### Do I need to be logged in to lucid.app?

Yes. It acts as you on lucid.app: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the lucid.app cookies saved by the Reduck extension.

### Does it change anything on lucid.app, or only read data?

It only reads. It looks things up on lucid.app and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/lucid.app/list_invoices, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/lucid.app/list_invoices

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/lucid.app/list_invoices
