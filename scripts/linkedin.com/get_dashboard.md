# Get LinkedIn dashboard analytics

Automatically get LinkedIn dashboard analytics on linkedin.com. Read the logged-in LinkedIn member's own analytics overview (Track performance): post impressions, total followers, profile viewers, search appearances, and newsletter rows when present. Returns one entry per tile with its value, percent change, direction (up/down/flat) and comparison window.

- Site: linkedin.com
- Address: `reduck/linkedin.com/get_dashboard`
- Updated: 2026-09-03 (v4)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/linkedin.com/get_dashboard`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/linkedin.com/get_dashboard
```

## Input

It takes no input.

## Output

- `metrics` (array, required)

## FAQ

### What does "Get LinkedIn dashboard analytics" do?

Read the logged-in LinkedIn member's own analytics overview (Track performance): post impressions, total followers, profile viewers, search appearances, and newsletter rows when present. Returns one entry per tile with its value, percent change, direction (up/down/flat) and comparison window.

### How do I automatically get LinkedIn dashboard analytics on linkedin.com?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/get_dashboard, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/get_dashboard

### Is there a linkedin.com API to get LinkedIn dashboard analytics?

You do not need one. "Get LinkedIn dashboard analytics" drives the real linkedin.com pages in a browser, so it works whether or not linkedin.com offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns metrics.

### Do I need to be logged in to linkedin.com?

Yes. It acts as you on linkedin.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the linkedin.com cookies saved by the Reduck extension.

### Does it change anything on linkedin.com, or only read data?

Unknown: its author has not declared whether it changes anything on linkedin.com, so treat it as if it could.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/get_dashboard, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/get_dashboard

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/linkedin.com/get_dashboard
