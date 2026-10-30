# Hugging Face — list invoices

Automatically list invoices on huggingface.co. List the signed-in Hugging Face account's billing invoices, newest first. Each row has the period, status and amount; hostedInvoiceUrl links to the downloadable invoice, or is null when Hugging Face shows none for that period. Reads the personal billing scope, not an organization's. Fails with a sign-in error when the browser is signed out of Hugging Face.

- Site: huggingface.co
- Address: `reduck/huggingface.co/list_invoices`
- Updated: 2026-10-29 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/huggingface.co/list_invoices`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/huggingface.co/list_invoices
```

## Input

It takes no input.

## Output

- `count` (integer, required)
- `invoices` (array, required)

## FAQ

### What does "Hugging Face — list invoices" do?

List the signed-in Hugging Face account's billing invoices, newest first. Each row has the period, status and amount; hostedInvoiceUrl links to the downloadable invoice, or is null when Hugging Face shows none for that period. Reads the personal billing scope, not an organization's. Fails with a sign-in error when the browser is signed out of Hugging Face.

### How do I automatically list invoices on huggingface.co?

Ask an AI agent connected to Reduck to run reduck/huggingface.co/list_invoices, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/huggingface.co/list_invoices

### Is there a huggingface.co API to list invoices?

You do not need one. "Hugging Face — list invoices" drives the real huggingface.co pages in a browser, so it works whether or not huggingface.co offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns count, invoices.

### Do I need to be logged in to huggingface.co?

Yes. It acts as you on huggingface.co: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the huggingface.co cookies saved by the Reduck extension.

### Does it change anything on huggingface.co, or only read data?

It only reads. It looks things up on huggingface.co and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/huggingface.co/list_invoices, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/huggingface.co/list_invoices

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/huggingface.co/list_invoices
