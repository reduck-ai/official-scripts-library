# Retest a monitor (Drata)

Re-runs one Drata monitoring test right away (the "Test now" button) instead of waiting for the daily check, then waits for the new result and returns the status before and after, with the failing and excluded resource counts. Takes the test number shown in the Drata UI (e.g. 7 for "Only Authorized Employees Change Code"). Requires being signed in to Drata.

- Site: drata.com
- Address: `reduck/drata.com/retest_monitor`
- Updated: 2026-10-09 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/drata.com/retest_monitor`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/drata.com/retest_monitor
```

## Input

- `testId` (integer, required): Test number as shown in the Drata UI (monitoring/production/<testId>/...), e.g. 7.
- `waitSeconds` (integer, optional): How long to wait for the retest to finish before returning (0 = trigger only).
- `workspaceId` (integer, optional): Drata workspace id. Defaults to the one the app opens (Conception AI = 1).

## Output

- `testId` (integer, required)
- `completed` (boolean, required): True when Drata finished the retest within waitSeconds.
- `triggered` (boolean, required)
- `name` (string | null, optional)
- `after` (object | null, optional)
- `before` (object | null, optional)

## FAQ

### What does "Retest a monitor (Drata)" do?

Re-runs one Drata monitoring test right away (the "Test now" button) instead of waiting for the daily check, then waits for the new result and returns the status before and after, with the failing and excluded resource counts. Takes the test number shown in the Drata UI (e.g. 7 for "Only Authorized Employees Change Code"). Requires being signed in to Drata.

### What information do I need to provide?

Required: testId. Optional: waitSeconds, workspaceId.

### What does it return?

It returns name, after, before, testId, completed, triggered.

### Do I need to be logged in to drata.com?

Yes. It acts as you on drata.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the drata.com cookies saved by the Reduck extension.

### Does it change anything on drata.com, or only read data?

It makes changes on drata.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/drata.com/retest_monitor, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/drata.com/retest_monitor

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/drata.com/retest_monitor
