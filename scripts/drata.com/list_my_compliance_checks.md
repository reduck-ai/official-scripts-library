# Drata: list my compliance checks

Automatically list my compliance checks on drata.com. List the signed-in employee's own Drata compliance checks (the items on the Drata employee hub): each check's type, pass/fail status, completion date, last check and expiry, plus totals. Read-only; changes nothing in Drata.

- Site: drata.com
- Address: `reduck/drata.com/list_my_compliance_checks`
- Updated: 2026-09-29 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/drata.com/list_my_compliance_checks`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/drata.com/list_my_compliance_checks
```

## Input

It takes no input.

## Output

- `total` (integer, required)
- `checks` (array, required)
- `passing` (integer, required)
- `startDate` (string | null, optional)
- `workspaceSlug` (string | null, optional)
- `employmentStatus` (string | null, optional)

## FAQ

### What does "Drata: list my compliance checks" do?

List the signed-in employee's own Drata compliance checks (the items on the Drata employee hub): each check's type, pass/fail status, completion date, last check and expiry, plus totals. Read-only; changes nothing in Drata.

### How do I automatically list my compliance checks on drata.com?

Ask an AI agent connected to Reduck to run reduck/drata.com/list_my_compliance_checks, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/drata.com/list_my_compliance_checks

### Is there a drata.com API to list my compliance checks?

You do not need one. "Drata: list my compliance checks" drives the real drata.com pages in a browser, so it works whether or not drata.com offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns total, checks, passing, startDate, workspaceSlug, employmentStatus.

### Do I need to be logged in to drata.com?

Yes. It acts as you on drata.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the drata.com cookies saved by the Reduck extension.

### Does it change anything on drata.com, or only read data?

It only reads. It looks things up on drata.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/drata.com/list_my_compliance_checks, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/drata.com/list_my_compliance_checks

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/drata.com/list_my_compliance_checks
