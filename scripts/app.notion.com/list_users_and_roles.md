# List Notion workspace members and guests

Automatically list Notion workspace members and guests on app.notion.com. List the email addresses of a Notion workspace's members and guests, along with the seat counters. Read-only — it changes nothing. Pass the optional email argument to also get a present true/false verdict, the quick way to confirm an offboarding landed. The full member list is returned, including the rows Notion only loads as you scroll. Acts on the workspace currently active in the browser, so there is no workspace name to pass. Requires being signed into Notion as a workspace owner.

- Site: app.notion.com
- Address: `reduck/app.notion.com/list_users_and_roles`
- Updated: 2026-08-10 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/app.notion.com/list_users_and_roles`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/app.notion.com/list_users_and_roles
```

## Input

- `email` (string, optional): Optional email to check for presence/absence among members and guests

## Output

- `guestEmails` (array, required)
- `memberEmails` (array, required)
- `present` (boolean | null, optional)
- `guestCount` (number | null, optional): Guest count as the workspace itself reports it
- `memberCount` (number | null, optional): Member count as the workspace itself reports it
- `checkedEmail` (string | null, optional)

## FAQ

### What does "List Notion workspace members and guests" do?

List the email addresses of a Notion workspace's members and guests, along with the seat counters. Read-only — it changes nothing. Pass the optional email argument to also get a present true/false verdict, the quick way to confirm an offboarding landed. The full member list is returned, including the rows Notion only loads as you scroll. Acts on the workspace currently active in the browser, so there is no workspace name to pass. Requires being signed into Notion as a workspace owner.

### How do I automatically list Notion workspace members and guests on app.notion.com?

Ask an AI agent connected to Reduck to run reduck/app.notion.com/list_users_and_roles, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/app.notion.com/list_users_and_roles

### Is there a app.notion.com API to list Notion workspace members and guests?

You do not need one. "List Notion workspace members and guests" drives the real app.notion.com pages in a browser, so it works whether or not app.notion.com offers an API for this.

### What information do I need to provide?

Optional: email.

### What does it return?

It returns present, guestCount, guestEmails, memberCount, checkedEmail, memberEmails.

### Do I need to be logged in to app.notion.com?

Yes. It acts as you on app.notion.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the app.notion.com cookies saved by the Reduck extension.

### Does it change anything on app.notion.com, or only read data?

It only reads. It looks things up on app.notion.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/app.notion.com/list_users_and_roles, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/app.notion.com/list_users_and_roles

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/app.notion.com/list_users_and_roles
