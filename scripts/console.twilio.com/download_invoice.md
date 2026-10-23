# Download Twilio receipt

Automatically download Twilio receipt on console.twilio.com. Download one month's Twilio payment receipt as a PDF file. Give the receipt id (receipt-YYYY-MM, as the Twilio invoice listing returns it) or just the month (YYYY-MM). Returns the month, its payment total, and the saved file's name with where it was saved (path on your own browser, or a link on a managed browser). A month without any payment has no receipt and is reported as such; a signed-out browser is reported too.

- Site: console.twilio.com
- Address: `reduck/console.twilio.com/download_invoice`
- Updated: 2026-10-22 (v8)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/console.twilio.com/download_invoice`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/console.twilio.com/download_invoice
```

## Input

- `invoiceId` (string, required): Receipt id from list_invoices, like receipt-2026-10 (a bare month 2026-10 also works).

## Output

- `month` (string, required): YYYY-MM of the receipt.
- `filename` (string, required): Name the file was saved under (may carry a ' (2)' suffix on repeats).
- `invoiceId` (string, required)
- `url` (string | null, optional): Link to the PDF when it is not on that machine (managed browser).
- `path` (string | null, optional): Where the PDF was saved on the machine running the browser (paired browser).
- `total` (string | null, optional): The month's payment total as Twilio displays it.
- `size_bytes` (integer, optional)

## FAQ

### What does "Download Twilio receipt" do?

Download one month's Twilio payment receipt as a PDF file. Give the receipt id (receipt-YYYY-MM, as the Twilio invoice listing returns it) or just the month (YYYY-MM). Returns the month, its payment total, and the saved file's name with where it was saved (path on your own browser, or a link on a managed browser). A month without any payment has no receipt and is reported as such; a signed-out browser is reported too.

### How do I automatically download Twilio receipt on console.twilio.com?

Ask an AI agent connected to Reduck to run reduck/console.twilio.com/download_invoice, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/console.twilio.com/download_invoice

### Is there a console.twilio.com API to download Twilio receipt?

You do not need one. "Download Twilio receipt" drives the real console.twilio.com pages in a browser, so it works whether or not console.twilio.com offers an API for this.

### What information do I need to provide?

Required: invoiceId.

### What does it return?

It returns url, path, month, total, filename, invoiceId, size_bytes.

### Do I need to be logged in to console.twilio.com?

Yes. It acts as you on console.twilio.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the console.twilio.com cookies saved by the Reduck extension.

### Does it change anything on console.twilio.com, or only read data?

It only reads. It looks things up on console.twilio.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/console.twilio.com/download_invoice, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/console.twilio.com/download_invoice

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/console.twilio.com/download_invoice
