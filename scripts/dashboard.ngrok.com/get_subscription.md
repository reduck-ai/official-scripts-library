# ngrok — get subscription

Automatically get subscription on dashboard.ngrok.com. Read the signed-in ngrok account's subscription: current plan, billing interval, renewal date, the plan scheduled for the next period, the current billing period, and the credit balance with its original grant and expiry. Read-only; signed out is a clear error.

- Site: dashboard.ngrok.com
- Address: `reduck/dashboard.ngrok.com/get_subscription`
- Updated: 2026-09-28 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/dashboard.ngrok.com/get_subscription`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/dashboard.ngrok.com/get_subscription
```

## Input

It takes no input.

## Output

- `plan` (string | null, required): ngrok's product id for the current plan, e.g. v3_free_monthly.
- `renewsAt` (string | null, optional)
- `scheduledPlan` (string | null, optional): Plan that takes effect at renewal (differs from plan when a change is pending).
- `intervalMonths` (integer | null, optional)
- `creditExpiresAt` (string | null, optional)
- `currentPeriodEnd` (string | null, optional)
- `creditBalanceCents` (integer | null, optional)
- `currentPeriodStart` (string | null, optional)
- `creditOriginalGrantCents` (integer | null, optional)

## FAQ

### What does "ngrok — get subscription" do?

Read the signed-in ngrok account's subscription: current plan, billing interval, renewal date, the plan scheduled for the next period, the current billing period, and the credit balance with its original grant and expiry. Read-only; signed out is a clear error.

### How do I automatically get subscription on dashboard.ngrok.com?

Ask an AI agent connected to Reduck to run reduck/dashboard.ngrok.com/get_subscription, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/dashboard.ngrok.com/get_subscription

### Is there a dashboard.ngrok.com API to get subscription?

You do not need one. "ngrok — get subscription" drives the real dashboard.ngrok.com pages in a browser, so it works whether or not dashboard.ngrok.com offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns plan, renewsAt, scheduledPlan, intervalMonths, creditExpiresAt, currentPeriodEnd, creditBalanceCents, currentPeriodStart, creditOriginalGrantCents.

### Do I need to be logged in to dashboard.ngrok.com?

Yes. It acts as you on dashboard.ngrok.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the dashboard.ngrok.com cookies saved by the Reduck extension.

### Does it change anything on dashboard.ngrok.com, or only read data?

It only reads. It looks things up on dashboard.ngrok.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/dashboard.ngrok.com/get_subscription, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/dashboard.ngrok.com/get_subscription

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/dashboard.ngrok.com/get_subscription
