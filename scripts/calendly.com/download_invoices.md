# Calendly API: download invoices

Automatically download invoices on calendly.com. Log into Calendly via Google SSO, list billing invoices, and download each invoice's PDF into the browser's download directory. Returns per invoice date, title, amount, currency, status, invoiceId, chargeId, filename and path (path is null when no PDF was available for that charge). Runs only on the browser extension, since it needs a native Google SSO session. Org admin only.

- Site: calendly.com
- Address: `reduck/calendly.com/download_invoices`
- Updated: 2026-09-18 (v10)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/calendly.com/download_invoices`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/calendly.com/download_invoices
```

## Input

- `email` (string, optional): Google account to pick in the SSO chooser, used only when a fresh sign-in is needed. If the browser already holds a Calendly session the chooser never appears, so this cannot be honoured — the run is then refused rather than silently returning whichever account is signed in. Omit it to read the session that is already active.

## Output

- `total` (integer, required): Number of invoices (charges) found.
- `invoices` (array, required)
- `attempted` (integer, required): How many of those invoices exposed a downloadUrl and so were actually attempted.
- `downloaded` (integer, required): How many PDFs were genuinely captured to disk (path non-null). When attempted > 0 and this is 0, the script throws instead of returning, because a download script that captured nothing has not done its job.

## FAQ

### What does "Calendly API: download invoices" do?

Log into Calendly via Google SSO, list billing invoices, and download each invoice's PDF into the browser's download directory. Returns per invoice date, title, amount, currency, status, invoiceId, chargeId, filename and path (path is null when no PDF was available for that charge). Runs only on the browser extension, since it needs a native Google SSO session. Org admin only.

### How do I automatically download invoices on calendly.com?

Ask an AI agent connected to Reduck to run reduck/calendly.com/download_invoices, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/calendly.com/download_invoices

### Is there a calendly.com API to download invoices?

You do not need one. "Calendly API: download invoices" drives the real calendly.com pages in a browser, so it works whether or not calendly.com offers an API for this.

### What information do I need to provide?

Optional: email.

### What does it return?

It returns total, invoices, attempted, downloaded.

### Do I need to be logged in to calendly.com?

Yes. It acts as you on calendly.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the calendly.com cookies saved by the Reduck extension.

### Does it change anything on calendly.com, or only read data?

It makes changes on calendly.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/calendly.com/download_invoices, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/calendly.com/download_invoices

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/calendly.com/download_invoices
