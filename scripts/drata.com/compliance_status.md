# Drata compliance status: failing tests, controls and personnel

Get everything currently failing in your Drata workspace in one call: the monitoring tests in failure with the date they started failing, the number of days since and the failing resources; the in-scope controls that are not ready with what they are missing; and the current personnel who are not compliant with the checks they fail. Needs a Drata session. Read-only: it changes nothing in Drata.

- Site: drata.com
- Address: `reduck/drata.com/compliance_status`
- Updated: 2026-10-09 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/drata.com/compliance_status`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/drata.com/compliance_status
```

## Input

- `sections` (array, optional): Which lists to return. Defaults to all three.
- `workspaceId` (integer, optional): Drata workspace id. Defaults to the workspace the app opens.

## Output

- `summary` (object, required)
- `checkedAt` (string, required)
- `workspaceId` (integer, required)
- `failingTests` (array, optional)
- `notReadyControls` (array, optional)
- `personnelInScope` (integer, optional)
- `nonCompliantPersonnel` (array, optional)

## FAQ

### What does "Drata compliance status: failing tests, controls and personnel" do?

Get everything currently failing in your Drata workspace in one call: the monitoring tests in failure with the date they started failing, the number of days since and the failing resources; the in-scope controls that are not ready with what they are missing; and the current personnel who are not compliant with the checks they fail. Needs a Drata session. Read-only: it changes nothing in Drata.

### What information do I need to provide?

Optional: sections, workspaceId.

### What does it return?

It returns summary, checkedAt, workspaceId, failingTests, notReadyControls, personnelInScope, nonCompliantPersonnel.

### Do I need to be logged in to drata.com?

Yes. It acts as you on drata.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the drata.com cookies saved by the Reduck extension.

### Does it change anything on drata.com, or only read data?

It only reads. It looks things up on drata.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/drata.com/compliance_status, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/drata.com/compliance_status

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/drata.com/compliance_status
