# List Welcome to the Jungle recruiter notifications

Automatically list Welcome to the Jungle recruiter notifications on welcomekit.co. List the recruiter dashboard notifications (bell feed) for a Welcome to the Jungle ATS org: new applications, candidate messages/emails and pipeline events. Returns each notification with its linked candidate, event type/label and modal path.

- Site: welcomekit.co
- Address: `reduck/welcomekit.co/list_notifications`
- Updated: 2026-07-29 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/welcomekit.co/list_notifications`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/welcomekit.co/list_notifications
```

## Input

- `org` (string, required): Organization reference as in the dashboard URL https://www.welcomekit.co/dashboard/o/<org>/ (6-char code, e.g. sfWkCZ).

## Output

- `org` (string, required)
- `count` (integer, required)
- `notifications` (array, required)

## FAQ

### What does "List Welcome to the Jungle recruiter notifications" do?

List the recruiter dashboard notifications (bell feed) for a Welcome to the Jungle ATS org: new applications, candidate messages/emails and pipeline events. Returns each notification with its linked candidate, event type/label and modal path.

### How do I automatically list Welcome to the Jungle recruiter notifications on welcomekit.co?

Ask an AI agent connected to Reduck to run reduck/welcomekit.co/list_notifications, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/welcomekit.co/list_notifications

### Is there a welcomekit.co API to list Welcome to the Jungle recruiter notifications?

You do not need one. "List Welcome to the Jungle recruiter notifications" drives the real welcomekit.co pages in a browser, so it works whether or not welcomekit.co offers an API for this.

### What information do I need to provide?

Required: org.

### What does it return?

It returns org, count, notifications.

### Do I need to be logged in to welcomekit.co?

Yes. It acts as you on welcomekit.co: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the welcomekit.co cookies saved by the Reduck extension.

### Does it change anything on welcomekit.co, or only read data?

Unknown: its author has not declared whether it changes anything on welcomekit.co, so treat it as if it could.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/welcomekit.co/list_notifications, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/welcomekit.co/list_notifications

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/welcomekit.co/list_notifications
