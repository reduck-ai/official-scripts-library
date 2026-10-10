# List expiring evidence (Drata)

Automatically list expiring evidence (Drata) on drata.com. Lists the Drata evidence library items that need attention: those whose renewal date falls within the next N days, those already expired, and optionally those that never received an artifact. For each item returns its name, status, renewal date and schedule, linked controls and a link to its page. Read-only.

- Site: drata.com
- Address: `reduck/drata.com/list_expiring_evidence`
- Updated: 2026-10-09 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/drata.com/list_expiring_evidence`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/drata.com/list_expiring_evidence
```

## Input

- `withinDays` (integer, optional): Include evidence whose renewal date is within this many days from today.
- `workspaceId` (integer, optional): Drata workspace id. Defaults to the one the app opens.
- `includeMissing` (boolean, optional): Also include evidence that never received an artifact (status NEEDS_SOURCE).

## Output

- `count` (integer, required)
- `items` (array, required)
- `totals` (object, required): Count of every evidence in the library by status.
- `checkedAt` (string, optional)

## FAQ

### What does "List expiring evidence (Drata)" do?

Lists the Drata evidence library items that need attention: those whose renewal date falls within the next N days, those already expired, and optionally those that never received an artifact. For each item returns its name, status, renewal date and schedule, linked controls and a link to its page. Read-only.

### How do I automatically list expiring evidence (Drata) on drata.com?

Ask an AI agent connected to Reduck to run reduck/drata.com/list_expiring_evidence, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/drata.com/list_expiring_evidence

### Is there a drata.com API to list expiring evidence (Drata)?

You do not need one. "List expiring evidence (Drata)" drives the real drata.com pages in a browser, so it works whether or not drata.com offers an API for this.

### What information do I need to provide?

Optional: withinDays, workspaceId, includeMissing.

### What does it return?

It returns count, items, totals, checkedAt.

### Do I need to be logged in to drata.com?

Yes. It acts as you on drata.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the drata.com cookies saved by the Reduck extension.

### Does it change anything on drata.com, or only read data?

It only reads. It looks things up on drata.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/drata.com/list_expiring_evidence, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/drata.com/list_expiring_evidence

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/drata.com/list_expiring_evidence
