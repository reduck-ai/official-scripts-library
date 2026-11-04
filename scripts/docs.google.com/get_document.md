# Google Docs: read a document

Automatically read a document on docs.google.com. Read a Google Doc the signed-in account can open: its title, its text, and its content in order as headings (with level), paragraphs, list items (with nesting depth and whether the list is numbered) and tables (cell by cell). Takes a document link or id. When the browser is signed in to several Google accounts, pass the account to read as.

- Site: docs.google.com
- Address: `reduck/docs.google.com/get_document`
- Updated: 2026-11-03 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/docs.google.com/get_document`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/docs.google.com/get_document
```

## Input

- `url` (string, required): Link to the Google Doc (https://docs.google.com/document/d/<id>/...) or the bare document id.
- `account` (string, optional): Google account to read as when the browser is signed in to several. Without it, Google Docs picks the account itself.

## Output

- `id` (string, required)
- `url` (string, required)
- `text` (string, required): The document's text, one line per paragraph, list item or table row (cells separated by tabs).
- `title` (string, required)
- `blocks` (array, required): The document's content in order.

## FAQ

### What does "Google Docs: read a document" do?

Read a Google Doc the signed-in account can open: its title, its text, and its content in order as headings (with level), paragraphs, list items (with nesting depth and whether the list is numbered) and tables (cell by cell). Takes a document link or id. When the browser is signed in to several Google accounts, pass the account to read as.

### How do I automatically read a document on docs.google.com?

Ask an AI agent connected to Reduck to run reduck/docs.google.com/get_document, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/docs.google.com/get_document

### Is there a docs.google.com API to read a document?

You do not need one. "Google Docs: read a document" drives the real docs.google.com pages in a browser, so it works whether or not docs.google.com offers an API for this.

### What information do I need to provide?

Required: url. Optional: account.

### What does it return?

It returns id, url, text, title, blocks.

### Do I need to be logged in to docs.google.com?

Yes. It acts as you on docs.google.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the docs.google.com cookies saved by the Reduck extension.

### Does it change anything on docs.google.com, or only read data?

It only reads. It looks things up on docs.google.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/docs.google.com/get_document, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/docs.google.com/get_document

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/docs.google.com/get_document
