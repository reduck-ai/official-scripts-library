# Download Uber trip receipt PDF

Automatically download Uber trip receipt PDF on riders.uber.com. Download one Uber trip's receipt as a PDF, by tripId (from riders.uber.com/list_trips). Returns the filename and the PDF bytes, base64-encoded (decode and write it yourself). Every completed trip has a receipt, including trips in regions that issue no separate VAT invoice; use riders.uber.com/download_invoice when you specifically need the VAT invoice document.

- Site: riders.uber.com
- Address: `reduck/riders.uber.com/download_receipt`
- Updated: 2026-09-21 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/riders.uber.com/download_receipt`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/riders.uber.com/download_receipt
```

## Input

- `tripId` (string, required): Trip uuid, e.g. cce57191-e89c-4200-84f7-451553bd95b6

## Output

- `filename` (string, required)
- `pdf_base64` (string, required): The PDF bytes, base64-encoded — decode and write to disk yourself.

## FAQ

### What does "Download Uber trip receipt PDF" do?

Download one Uber trip's receipt as a PDF, by tripId (from riders.uber.com/list_trips). Returns the filename and the PDF bytes, base64-encoded (decode and write it yourself). Every completed trip has a receipt, including trips in regions that issue no separate VAT invoice; use riders.uber.com/download_invoice when you specifically need the VAT invoice document.

### How do I automatically download Uber trip receipt PDF on riders.uber.com?

Ask an AI agent connected to Reduck to run reduck/riders.uber.com/download_receipt, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/riders.uber.com/download_receipt

### Is there a riders.uber.com API to download Uber trip receipt PDF?

You do not need one. "Download Uber trip receipt PDF" drives the real riders.uber.com pages in a browser, so it works whether or not riders.uber.com offers an API for this.

### What information do I need to provide?

Required: tripId.

### What does it return?

It returns filename, pdf_base64.

### Do I need to be logged in to riders.uber.com?

Yes. It acts as you on riders.uber.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the riders.uber.com cookies saved by the Reduck extension.

### Does it change anything on riders.uber.com, or only read data?

It only reads. It looks things up on riders.uber.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/riders.uber.com/download_receipt, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/riders.uber.com/download_receipt

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/riders.uber.com/download_receipt
