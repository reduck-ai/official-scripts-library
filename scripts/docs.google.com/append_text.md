# Google Docs: add text at the end of a document

Automatically add text at the end of a document on docs.google.com. Add text at the end of a Google Doc you can edit, then read the document back to confirm it. Each line becomes a paragraph after the last one, added exactly as given (no automatic lists or curly quotes). Refuses when the account can only view or the document is in Suggesting mode. When the browser is signed in to several Google accounts, pass the account to act as.

- Site: docs.google.com
- Address: `reduck/docs.google.com/append_text`
- Updated: 2026-11-03 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/docs.google.com/append_text`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/docs.google.com/append_text
```

## Input

- `url` (string, required): Link to the Google Doc (https://docs.google.com/document/d/<id>/...) or the bare document id.
- `text` (string, required): Text to add. Each line becomes its own paragraph after the document's last one. It is added as given: quotes stay straight and lines starting with - or 1. stay plain text, not lists.
- `account` (string, optional): Google account to act as when the browser is signed in to several. Without it, Google Docs picks the account itself (usually the one used last), and the result says which one it was.

## Output

- `id` (string, required)
- `url` (string, required)
- `added` (array, required): The paragraphs added, as read back from the document.
- `title` (string, required)
- `verified` (boolean, required): True when the document, read back after the edit, ends with the given lines.
- `accountUsed` (string | null, required): Email of the Google account the editor was signed in as.

## FAQ

### What does "Google Docs: add text at the end of a document" do?

Add text at the end of a Google Doc you can edit, then read the document back to confirm it. Each line becomes a paragraph after the last one, added exactly as given (no automatic lists or curly quotes). Refuses when the account can only view or the document is in Suggesting mode. When the browser is signed in to several Google accounts, pass the account to act as.

### How do I automatically add text at the end of a document on docs.google.com?

Ask an AI agent connected to Reduck to run reduck/docs.google.com/append_text, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/docs.google.com/append_text

### Is there a docs.google.com API to add text at the end of a document?

You do not need one. "Google Docs: add text at the end of a document" drives the real docs.google.com pages in a browser, so it works whether or not docs.google.com offers an API for this.

### What information do I need to provide?

Required: url, text. Optional: account.

### What does it return?

It returns id, url, added, title, verified, accountUsed.

### Do I need to be logged in to docs.google.com?

Yes. It acts as you on docs.google.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the docs.google.com cookies saved by the Reduck extension.

### Does it change anything on docs.google.com, or only read data?

It makes changes on docs.google.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/docs.google.com/append_text, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/docs.google.com/append_text

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/docs.google.com/append_text
