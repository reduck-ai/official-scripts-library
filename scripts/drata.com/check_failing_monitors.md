# List failing Drata monitoring tests

Automatically list failing Drata monitoring tests on drata.com. List the Drata monitoring tests that are currently failing in production, each with its failing resources or people: name, account, region and severity, plus how many findings and exclusions it has. Needs a Drata session. Read-only: it changes nothing in Drata.

- Site: drata.com
- Address: `reduck/drata.com/check_failing_monitors`
- Updated: 2026-10-08 (v4)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/drata.com/check_failing_monitors`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/drata.com/check_failing_monitors
```

## Input

- `workspaceId` (integer, optional): Drata workspace id. Defaults to the workspace the app opens.
- `includeFindings` (boolean, optional): Also fetch the failing resources (findings) of each failing test.

## Output

- `tests` (array, required)
- `failingCount` (integer, required)
- `checkedAt` (string, optional)

## FAQ

### What does "List failing Drata monitoring tests" do?

List the Drata monitoring tests that are currently failing in production, each with its failing resources or people: name, account, region and severity, plus how many findings and exclusions it has. Needs a Drata session. Read-only: it changes nothing in Drata.

### How do I automatically list failing Drata monitoring tests on drata.com?

Ask an AI agent connected to Reduck to run reduck/drata.com/check_failing_monitors, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/drata.com/check_failing_monitors

### Is there a drata.com API to list failing Drata monitoring tests?

You do not need one. "List failing Drata monitoring tests" drives the real drata.com pages in a browser, so it works whether or not drata.com offers an API for this.

### What information do I need to provide?

Optional: workspaceId, includeFindings.

### What does it return?

It returns tests, checkedAt, failingCount.

### Do I need to be logged in to drata.com?

Yes. It acts as you on drata.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the drata.com cookies saved by the Reduck extension.

### Does it change anything on drata.com, or only read data?

It only reads. It looks things up on drata.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/drata.com/check_failing_monitors, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/drata.com/check_failing_monitors

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/drata.com/check_failing_monitors
