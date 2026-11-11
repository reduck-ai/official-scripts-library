# Google Drive: list documents waiting for signature

Automatically list documents waiting for signature on docs.google.com. List the Google Drive / Docs files with an open signature or approval request: those waiting for the signed-in account to sign (default), or those the account sent out. Each item has the file id, title and the link to sign it; pass the link to sign_document. Returns an empty list when nothing is waiting. Reads the first screen of Drive's results (about 50 files). When the browser is signed in to several Google accounts, pass the account to act as.

- Site: docs.google.com
- Address: `reduck/docs.google.com/list_signature_requests`
- Updated: 2026-11-10 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/docs.google.com/list_signature_requests`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/docs.google.com/list_signature_requests
```

## Input

- `which` (string, optional): to_sign: requests waiting for this account to sign or approve. sent: requests this account sent out.
- `account` (string, optional): Google account to act as when the browser is signed in to several.

## Output

- `items` (array, required)
- `which` (string, required)
- `account` (string | null, optional)

## FAQ

### What does "Google Drive: list documents waiting for signature" do?

List the Google Drive / Docs files with an open signature or approval request: those waiting for the signed-in account to sign (default), or those the account sent out. Each item has the file id, title and the link to sign it; pass the link to sign_document. Returns an empty list when nothing is waiting. Reads the first screen of Drive's results (about 50 files). When the browser is signed in to several Google accounts, pass the account to act as.

### How do I automatically list documents waiting for signature on docs.google.com?

Ask an AI agent connected to Reduck to run reduck/docs.google.com/list_signature_requests, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/docs.google.com/list_signature_requests

### Is there a docs.google.com API to list documents waiting for signature?

You do not need one. "Google Drive: list documents waiting for signature" drives the real docs.google.com pages in a browser, so it works whether or not docs.google.com offers an API for this.

### What information do I need to provide?

Optional: which, account.

### What does it return?

It returns items, which, account.

### Do I need to be logged in to docs.google.com?

Yes. It acts as you on docs.google.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the docs.google.com cookies saved by the Reduck extension.

### Does it change anything on docs.google.com, or only read data?

It only reads. It looks things up on docs.google.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/docs.google.com/list_signature_requests, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/docs.google.com/list_signature_requests

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/docs.google.com/list_signature_requests
