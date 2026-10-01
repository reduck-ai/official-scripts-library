# DocuSign — delete a draft envelope

Automatically delete a draft envelope on docusign.com. Delete a draft envelope from the signed-in DocuSign account by its envelope id. The draft moves to Deleted Items. Only unsent drafts from the last 6 months shown on the first page of Drafts can be deleted, and a dry run opens the confirmation without deleting. Signed out is a clear error.

- Site: docusign.com
- Address: `reduck/docusign.com/delete_draft`
- Updated: 2026-09-30 (v6)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/docusign.com/delete_draft`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/docusign.com/delete_draft
```

## Input

- `envelopeId` (string, required): Id of the draft envelope to delete (e.g. from docusign.com/upload_document).
- `dryRun` (boolean, optional): Find the draft and open the delete confirmation, then stop without deleting.

## Output

- `dryRun` (boolean, required)
- `deleted` (boolean, required)
- `envelopeId` (string, required)
- `name` (string | null, optional)
- `movedTo` (string | null, optional)

## FAQ

### What does "DocuSign — delete a draft envelope" do?

Delete a draft envelope from the signed-in DocuSign account by its envelope id. The draft moves to Deleted Items. Only unsent drafts from the last 6 months shown on the first page of Drafts can be deleted, and a dry run opens the confirmation without deleting. Signed out is a clear error.

### How do I automatically delete a draft envelope on docusign.com?

Ask an AI agent connected to Reduck to run reduck/docusign.com/delete_draft, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/docusign.com/delete_draft

### Is there a docusign.com API to delete a draft envelope?

You do not need one. "DocuSign — delete a draft envelope" drives the real docusign.com pages in a browser, so it works whether or not docusign.com offers an API for this.

### What information do I need to provide?

Required: envelopeId. Optional: dryRun.

### What does it return?

It returns name, dryRun, deleted, movedTo, envelopeId.

### Do I need to be logged in to docusign.com?

Yes. It acts as you on docusign.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the docusign.com cookies saved by the Reduck extension.

### Does it change anything on docusign.com, or only read data?

It makes changes on docusign.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/docusign.com/delete_draft, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/docusign.com/delete_draft

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/docusign.com/delete_draft
