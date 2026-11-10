# Google Docs: create a document

Automatically create a document on docs.google.com. Create a new Google Doc in the signed-in account's Drive, with a title and optional text, and return its id, link and the account it was created in. Each line of the text becomes a paragraph, added exactly as given (no automatic lists or curly quotes). When the browser is signed in to several Google accounts, pass the account to create it in; otherwise Google Docs picks one.

- Site: docs.google.com
- Address: `reduck/docs.google.com/create_document`
- Updated: 2026-11-09 (v4)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/docs.google.com/create_document`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/docs.google.com/create_document
```

## Input

- `title` (string, required): The document's title.
- `text` (string, optional): Text for the document's body. Each line becomes its own paragraph, added as given: quotes stay straight and lines starting with - or 1. stay plain text, not lists. Leave it out for an empty document.
- `account` (string, optional): Google account to create the document in when the browser is signed in to several. Without it, Google Docs picks the account itself (usually the one used last), and the result says which one it was.

## Output

- `id` (string, required): The new document's id; pass it to get_document or append_text.
- `url` (string, required)
- `text` (string, required): The document's body as read back, one line per paragraph.
- `title` (string, required): The title as read back from the document.
- `verified` (boolean, required): True when the document, read back, has the given title and text.
- `accountUsed` (string | null, required): Email of the Google account the document was created in.

## FAQ

### What does "Google Docs: create a document" do?

Create a new Google Doc in the signed-in account's Drive, with a title and optional text, and return its id, link and the account it was created in. Each line of the text becomes a paragraph, added exactly as given (no automatic lists or curly quotes). When the browser is signed in to several Google accounts, pass the account to create it in; otherwise Google Docs picks one.

### How do I automatically create a document on docs.google.com?

Ask an AI agent connected to Reduck to run reduck/docs.google.com/create_document, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/docs.google.com/create_document

### Is there a docs.google.com API to create a document?

You do not need one. "Google Docs: create a document" drives the real docs.google.com pages in a browser, so it works whether or not docs.google.com offers an API for this.

### What information do I need to provide?

Required: title. Optional: text, account.

### What does it return?

It returns id, url, text, title, verified, accountUsed.

### Do I need to be logged in to docs.google.com?

Yes. It acts as you on docs.google.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the docs.google.com cookies saved by the Reduck extension.

### Does it change anything on docs.google.com, or only read data?

It makes changes on docs.google.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/docs.google.com/create_document, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/docs.google.com/create_document

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/docs.google.com/create_document
