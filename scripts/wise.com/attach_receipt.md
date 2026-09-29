# Attach a receipt to a Wise transaction

Automatically attach a receipt to a Wise transaction on wise.com. Attach a receipt or invoice (PDF, JPG, PNG…, under 10MB) to a Wise card transaction, given its card transaction id (from search_transactions). The file is passed as base64 with an optional filename and MIME type (default receipt.pdf, application/pdf). The attachment is confirmed from Wise's own upload response. This is a write: the file stays on the transaction.

- Site: wise.com
- Address: `reduck/wise.com/attach_receipt`
- Updated: 2026-09-28 (v6)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/wise.com/attach_receipt`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/wise.com/attach_receipt
```

## Input

- `b64` (string, required): Contenu du fichier encodé en base64.
- `txid` (string, required): L'id CARD_TRANSACTION Wise (ex: 2980039980).
- `mime` (string, optional): Type MIME (défaut application/pdf).
- `filename` (string, optional): Nom du fichier (défaut receipt.pdf).

## Output

- `txid` (string, required)
- `attached` (boolean, required)
- `attachmentSection` (string, optional)

## FAQ

### What does "Attach a receipt to a Wise transaction" do?

Attach a receipt or invoice (PDF, JPG, PNG…, under 10MB) to a Wise card transaction, given its card transaction id (from search_transactions). The file is passed as base64 with an optional filename and MIME type (default receipt.pdf, application/pdf). The attachment is confirmed from Wise's own upload response. This is a write: the file stays on the transaction.

### How do I automatically attach a receipt to a Wise transaction on wise.com?

Ask an AI agent connected to Reduck to run reduck/wise.com/attach_receipt, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/wise.com/attach_receipt

### Is there a wise.com API to attach a receipt to a Wise transaction?

You do not need one. "Attach a receipt to a Wise transaction" drives the real wise.com pages in a browser, so it works whether or not wise.com offers an API for this.

### What information do I need to provide?

Required: txid, b64. Optional: mime, filename.

### What does it return?

It returns txid, attached, attachmentSection.

### Do I need to be logged in to wise.com?

Yes. It acts as you on wise.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the wise.com cookies saved by the Reduck extension.

### Does it change anything on wise.com, or only read data?

Unknown: its author has not declared whether it changes anything on wise.com, so treat it as if it could.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/wise.com/attach_receipt, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/wise.com/attach_receipt

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/wise.com/attach_receipt
