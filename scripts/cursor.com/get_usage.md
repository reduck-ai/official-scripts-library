# Cursor — get usage

Automatically get usage on cursor.com. Read the signed-in Cursor account's usage for the current billing cycle: cycle start and end, plan name and price, membership type, percent of included usage used (total, Auto model, API/named models), included usage used / limit / remaining with its breakdown, on-demand (usage-based) spending, and team on-demand usage for team plans. Read-only; signed out is a clear error.

- Site: cursor.com
- Address: `reduck/cursor.com/get_usage`
- Updated: 2026-09-28 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/cursor.com/get_usage`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/cursor.com/get_usage
```

## Input

It takes no input.

## Output

- `membershipType` (string | null, required)
- `billingCycleEnd` (string | null, required)
- `billingCycleStart` (string | null, required)
- `included` (object | null, optional): The plan's included usage as Cursor reports it: used, limit, remaining and breakdown (included / bonus / total), in Cursor's own units.
- `onDemand` (object | null, optional): Usage-based (on-demand) spending: enabled, used, limit, remaining.
- `planName` (string | null, optional)
- `planPrice` (string | null, optional)
- `teamUsage` (object | null, optional)
- `isUnlimited` (boolean | null, optional)
- `percentUsed` (object, optional)

## FAQ

### What does "Cursor — get usage" do?

Read the signed-in Cursor account's usage for the current billing cycle: cycle start and end, plan name and price, membership type, percent of included usage used (total, Auto model, API/named models), included usage used / limit / remaining with its breakdown, on-demand (usage-based) spending, and team on-demand usage for team plans. Read-only; signed out is a clear error.

### How do I automatically get usage on cursor.com?

Ask an AI agent connected to Reduck to run reduck/cursor.com/get_usage, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/cursor.com/get_usage

### Is there a cursor.com API to get usage?

You do not need one. "Cursor — get usage" drives the real cursor.com pages in a browser, so it works whether or not cursor.com offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns included, onDemand, planName, planPrice, teamUsage, isUnlimited, percentUsed, membershipType, billingCycleEnd, billingCycleStart.

### Do I need to be logged in to cursor.com?

Yes. It acts as you on cursor.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the cursor.com cookies saved by the Reduck extension.

### Does it change anything on cursor.com, or only read data?

It only reads. It looks things up on cursor.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/cursor.com/get_usage, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/cursor.com/get_usage

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/cursor.com/get_usage
