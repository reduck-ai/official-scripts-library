# Invite workspace member (Notion)

Automatically invite workspace member (Notion) on app.notion.com. Invite someone to a Notion workspace by email, with a chosen role and built-in verification. Records the People page before and after, returning invited / verified — proof the invite actually landed. dryRun (default true) fills the invite form and cancels without sending; set it to false to actually send the invite. Role defaults to "Restricted member" (available on all plans); "Workspace owner" is also supported. The "Member" role requires a paid Notion Plus plan and is rejected up front rather than silently opening a billing/upgrade dialog. Acts on the workspace currently active in the browser, so there is no workspace name to pass. Requires being signed into Notion with permission to invite members.

- Site: app.notion.com
- Address: `reduck/app.notion.com/add_member`
- Updated: 2026-09-08 (v25)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/app.notion.com/add_member`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/app.notion.com/add_member
```

## Input

- `email` (string, required): Email address to invite
- `role` (string, optional): Role to grant. Default "Restricted member". "Member" is not supported here — it requires a paid Notion Plus plan/seat and would otherwise open a billing dialog.
- `dryRun` (boolean, optional): If true (default), fills the invite form then clicks Cancel without sending. Set false to actually send the invite.
- `message` (string, optional): Optional note to include with the invite

## Output

- `role` (string, required)
- `sent` (boolean, required)
- `email` (string, required)
- `dryRun` (boolean, required)
- `after` (object, optional)
- `found` (boolean, optional)
- `before` (object, optional)
- `foundIn` (string | null, optional)
- `verifiedNoInvite` (boolean, optional)

## FAQ

### What does "Invite workspace member (Notion)" do?

Invite someone to a Notion workspace by email, with a chosen role and built-in verification. Records the People page before and after, returning invited / verified — proof the invite actually landed. dryRun (default true) fills the invite form and cancels without sending; set it to false to actually send the invite. Role defaults to "Restricted member" (available on all plans); "Workspace owner" is also supported. The "Member" role requires a paid Notion Plus plan and is rejected up front rather than silently opening a billing/upgrade dialog. Acts on the workspace currently active in the browser, so there is no workspace name to pass. Requires being signed into Notion with permission to invite members.

### How do I automatically invite workspace member (Notion) on app.notion.com?

Ask an AI agent connected to Reduck to run reduck/app.notion.com/add_member, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/app.notion.com/add_member

### Is there a app.notion.com API to invite workspace member (Notion)?

You do not need one. "Invite workspace member (Notion)" drives the real app.notion.com pages in a browser, so it works whether or not app.notion.com offers an API for this.

### What information do I need to provide?

Required: email. Optional: role, dryRun, message.

### What does it return?

It returns role, sent, after, email, found, before, dryRun, foundIn, verifiedNoInvite.

### Do I need to be logged in to app.notion.com?

Yes. It acts as you on app.notion.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the app.notion.com cookies saved by the Reduck extension.

### Does it change anything on app.notion.com, or only read data?

It makes changes on app.notion.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/app.notion.com/add_member, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/app.notion.com/add_member

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/app.notion.com/add_member
