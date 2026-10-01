# DocuSign — list envelopes

Automatically list envelopes on docusign.com. List the envelopes (documents sent for signature) on the signed-in DocuSign account's Agreements page — the last 6 months, first page: each envelope's id, subject, status, sender, and created / sent / completed / last-modified dates — plus the account's folders (Drafts, Inbox, Sent, Deleted…) with their item counts. Read-only; signed out is a clear error. An account with no envelopes returns an empty list.

- Site: docusign.com
- Address: `reduck/docusign.com/list_envelopes`
- Updated: 2026-09-30 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/docusign.com/list_envelopes`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/docusign.com/list_envelopes
```

## Input

It takes no input.

## Output

- `total` (integer, required)
- `folders` (array, required)
- `envelopes` (array, required)

## FAQ

### What does "DocuSign — list envelopes" do?

List the envelopes (documents sent for signature) on the signed-in DocuSign account's Agreements page — the last 6 months, first page: each envelope's id, subject, status, sender, and created / sent / completed / last-modified dates — plus the account's folders (Drafts, Inbox, Sent, Deleted…) with their item counts. Read-only; signed out is a clear error. An account with no envelopes returns an empty list.

### How do I automatically list envelopes on docusign.com?

Ask an AI agent connected to Reduck to run reduck/docusign.com/list_envelopes, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/docusign.com/list_envelopes

### Is there a docusign.com API to list envelopes?

You do not need one. "DocuSign — list envelopes" drives the real docusign.com pages in a browser, so it works whether or not docusign.com offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns total, folders, envelopes.

### Do I need to be logged in to docusign.com?

Yes. It acts as you on docusign.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the docusign.com cookies saved by the Reduck extension.

### Does it change anything on docusign.com, or only read data?

It only reads. It looks things up on docusign.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/docusign.com/list_envelopes, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/docusign.com/list_envelopes

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/docusign.com/list_envelopes
