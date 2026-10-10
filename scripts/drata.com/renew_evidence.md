# Renew an evidence with a new file (Drata)

Uploads a new file to an evidence of the Drata evidence library, making it the current artifact and moving the previous one to past artifacts. Sets the creation date (today by default); Drata computes the next renewal date from the evidence's schedule. Returns the new current artifact with its creation and renewal dates. Requires being signed in to Drata.

- Site: drata.com
- Address: `reduck/drata.com/renew_evidence`
- Updated: 2026-10-09 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/drata.com/renew_evidence`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/drata.com/renew_evidence
```

## Input

- `file` (string, required): The new artifact file (PDF, PNG, DOCX, XLSX, CSV, TXT, ZIP...).
- `fileName` (string, required): Name the file gets in Drata, with its extension, e.g. dependabot-2026-q4.png.
- `evidenceId` (integer, required): Evidence id, as in .../compliance/evidence/<id>/current-artifacts (list_expiring_evidence returns it).
- `creationDate` (string, optional): Artifact creation date, yyyy-mm-dd. Defaults to today.
- `workspacePath` (string, optional): Workspace path of the app URL. Defaults to the one the app opens.

## Output

- `renewed` (boolean, required)
- `evidenceId` (integer, required)
- `status` (string | null, optional)
- `current` (object | null, optional)
- `evidenceName` (string | null, optional)

## FAQ

### What does "Renew an evidence with a new file (Drata)" do?

Uploads a new file to an evidence of the Drata evidence library, making it the current artifact and moving the previous one to past artifacts. Sets the creation date (today by default); Drata computes the next renewal date from the evidence's schedule. Returns the new current artifact with its creation and renewal dates. Requires being signed in to Drata.

### What information do I need to provide?

Required: evidenceId, file, fileName. Optional: creationDate, workspacePath.

### What does it return?

It returns status, current, renewed, evidenceId, evidenceName.

### Do I need to be logged in to drata.com?

Yes. It acts as you on drata.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the drata.com cookies saved by the Reduck extension.

### Does it change anything on drata.com, or only read data?

It makes changes on drata.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/drata.com/renew_evidence, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/drata.com/renew_evidence

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/drata.com/renew_evidence
