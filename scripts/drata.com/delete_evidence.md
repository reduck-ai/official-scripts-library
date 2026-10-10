# Delete an evidence (Drata)

Automatically delete an evidence (Drata) on drata.com. Permanently deletes one evidence from the Drata evidence library, with all its current and past artifacts; this cannot be undone. Always run it first as a dry run (the default), show the user the evidence name and id it found, and only run it with dryRun false after the user has explicitly confirmed that deletion. The caller must also pass the evidence's exact name, which is checked against the page before anything is deleted. Requires being signed in to Drata.

- Site: drata.com
- Address: `reduck/drata.com/delete_evidence`
- Updated: 2026-10-09 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/drata.com/delete_evidence`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/drata.com/delete_evidence
```

## Input

- `evidenceId` (integer, required): Evidence id, as in .../compliance/evidence/<id>/overview.
- `expectedName` (string, required): Exact name of the evidence. The script refuses to delete if the page shows another name.
- `dryRun` (boolean, optional): true (default) opens the confirmation and cancels; false deletes. Only pass false after the user has explicitly confirmed this deletion.
- `workspacePath` (string, optional): Workspace path of the app URL. Defaults to the one the app opens.

## Output

- `name` (string, required)
- `dryRun` (boolean, required)
- `deleted` (boolean, required): true only when the evidence is confirmed gone from the library.
- `evidenceId` (integer, required)

## FAQ

### What does "Delete an evidence (Drata)" do?

Permanently deletes one evidence from the Drata evidence library, with all its current and past artifacts; this cannot be undone. Always run it first as a dry run (the default), show the user the evidence name and id it found, and only run it with dryRun false after the user has explicitly confirmed that deletion. The caller must also pass the evidence's exact name, which is checked against the page before anything is deleted. Requires being signed in to Drata.

### How do I automatically delete an evidence (Drata) on drata.com?

Ask an AI agent connected to Reduck to run reduck/drata.com/delete_evidence, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/drata.com/delete_evidence

### Is there a drata.com API to delete an evidence (Drata)?

You do not need one. "Delete an evidence (Drata)" drives the real drata.com pages in a browser, so it works whether or not drata.com offers an API for this.

### What information do I need to provide?

Required: evidenceId, expectedName. Optional: dryRun, workspacePath.

### What does it return?

It returns name, dryRun, deleted, evidenceId.

### Do I need to be logged in to drata.com?

Yes. It acts as you on drata.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the drata.com cookies saved by the Reduck extension.

### Does it change anything on drata.com, or only read data?

It makes changes on drata.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/drata.com/delete_evidence, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/drata.com/delete_evidence

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/drata.com/delete_evidence
