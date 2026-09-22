# Invite Asana team member

Automatically invite Asana team member on asana.com. Invite a person into an Asana team by email, via Team Settings > Members > "Invite to team". New invites join as Member (guests from outside the org's domain cannot be made Team admin at invite time — use change_role afterward for domain members). Requires login and team-admin permission.

- Site: asana.com
- Address: `reduck/asana.com/create_user`
- Updated: 2026-08-20 (v13)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/asana.com/create_user`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/asana.com/create_user
```

## Input

- `email` (string, required): Email address to invite into the team. Must be a well-formed address — Asana's UI silently autocompletes bare usernames to '<input>@<org-domain>', so malformed input is rejected rather than sending an unintended invite.
- `teamName` (string, required): Team name as shown in the sidebar (case-insensitive substring match).

## Output

- `team` (string, required)
- `email` (string, required)
- `invited` (boolean, required)

## FAQ

### What does "Invite Asana team member" do?

Invite a person into an Asana team by email, via Team Settings > Members > "Invite to team". New invites join as Member (guests from outside the org's domain cannot be made Team admin at invite time — use change_role afterward for domain members). Requires login and team-admin permission.

### How do I automatically invite Asana team member on asana.com?

Ask an AI agent connected to Reduck to run reduck/asana.com/create_user, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/asana.com/create_user

### Is there a asana.com API to invite Asana team member?

You do not need one. "Invite Asana team member" drives the real asana.com pages in a browser, so it works whether or not asana.com offers an API for this.

### What information do I need to provide?

Required: teamName, email.

### What does it return?

It returns team, email, invited.

### Do I need to be logged in to asana.com?

Yes. It acts as you on asana.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the asana.com cookies saved by the Reduck extension.

### Does it change anything on asana.com, or only read data?

It makes changes on asana.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/asana.com/create_user, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/asana.com/create_user

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/asana.com/create_user
