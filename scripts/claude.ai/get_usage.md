# Claude.ai plan usage

Read the signed-in Claude.ai account's plan usage, as Settings > Usage shows it for the organisation the browser has open: every limit (current 5-hour session, weekly all models, weekly per model) with its percent used, severity, reset time (ISO) and whether it is the one currently binding; the raw five_hour and seven_day utilization; the weekly split by surface (Claude Code, chats, Cowork); and the usage-credits state. Read-only. A signed-out browser fails with an error that says to sign in; an account that has not finished onboarding, or a Free plan with no usage settings, fails with an error that says so; a refused or rate-limited usage request fails within seconds with the HTTP status.

- Site: claude.ai
- Address: `reduck/claude.ai/get_usage`
- Updated: 2026-10-22 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/claude.ai/get_usage`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/claude.ai/get_usage
```

## Input

It takes no input.

## Output

- `limits` (array, required)
- `readAt` (string, required)
- `orgUuid` (string, required)
- `fiveHour` (object | null, required)
- `sevenDay` (object | null, required)
- `extraUsage` (object | null, required)
- `weeklyBreakdown` (array, required)

## FAQ

### What does "Claude.ai plan usage" do?

Read the signed-in Claude.ai account's plan usage, as Settings > Usage shows it for the organisation the browser has open: every limit (current 5-hour session, weekly all models, weekly per model) with its percent used, severity, reset time (ISO) and whether it is the one currently binding; the raw five_hour and seven_day utilization; the weekly split by surface (Claude Code, chats, Cowork); and the usage-credits state. Read-only. A signed-out browser fails with an error that says to sign in; an account that has not finished onboarding, or a Free plan with no usage settings, fails with an error that says so; a refused or rate-limited usage request fails within seconds with the HTTP status.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns limits, readAt, orgUuid, fiveHour, sevenDay, extraUsage, weeklyBreakdown.

### Do I need to be logged in to claude.ai?

Yes. It acts as you on claude.ai: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the claude.ai cookies saved by the Reduck extension.

### Does it change anything on claude.ai, or only read data?

It only reads. It looks things up on claude.ai and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/claude.ai/get_usage, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/claude.ai/get_usage

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/claude.ai/get_usage
