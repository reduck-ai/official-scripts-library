# Browserbase — get usage

Automatically get usage on browserbase.com. Read a Browserbase project's usage — browser time (ms), proxy bytes, agent runs, fetch and search requests and model-gateway spend (microcents) — as totals, averages and per-day buckets, for the current billing period or the last 7 or 30 days. org and projectId default to the dashboard's own (see browserbase.com/list_projects). Read-only; signed out is a clear error.

- Site: browserbase.com
- Address: `reduck/browserbase.com/get_usage`
- Updated: 2026-09-28 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/browserbase.com/get_usage`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/browserbase.com/get_usage
```

## Input

- `org` (string, optional): Org slug (from browserbase.com/whoami). Omit for the default org.
- `range` (string, optional): Time window. Default current-period (the billing period so far).
- `projectId` (string, optional): Project id (from browserbase.com/list_projects). Omit for the org's default project.

## Output

- `org` (string, required)
- `range` (string, required)
- `totals` (object, required)
- `projectId` (string, required)
- `buckets` (array, optional)
- `averages` (object | null, optional)
- `windowEnd` (string | null, optional)
- `windowStart` (string | null, optional)

## FAQ

### What does "Browserbase — get usage" do?

Read a Browserbase project's usage — browser time (ms), proxy bytes, agent runs, fetch and search requests and model-gateway spend (microcents) — as totals, averages and per-day buckets, for the current billing period or the last 7 or 30 days. org and projectId default to the dashboard's own (see browserbase.com/list_projects). Read-only; signed out is a clear error.

### How do I automatically get usage on browserbase.com?

Ask an AI agent connected to Reduck to run reduck/browserbase.com/get_usage, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/browserbase.com/get_usage

### Is there a browserbase.com API to get usage?

You do not need one. "Browserbase — get usage" drives the real browserbase.com pages in a browser, so it works whether or not browserbase.com offers an API for this.

### What information do I need to provide?

Optional: org, range, projectId.

### What does it return?

It returns org, range, totals, buckets, averages, projectId, windowEnd, windowStart.

### Do I need to be logged in to browserbase.com?

Yes. It acts as you on browserbase.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the browserbase.com cookies saved by the Reduck extension.

### Does it change anything on browserbase.com, or only read data?

It only reads. It looks things up on browserbase.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/browserbase.com/get_usage, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/browserbase.com/get_usage

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/browserbase.com/get_usage
