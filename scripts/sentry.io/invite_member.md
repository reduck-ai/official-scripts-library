# Invite a member to a Sentry organization

Automatically invite a member to a Sentry organization on sentry.io. Invites one person by email to a Sentry organization with a given role, optionally adding them to teams. Returns the pending member that Sentry created. Fails with a clear message when the signed-in account may not invite members or the email is already a member.

- Site: sentry.io
- Address: `reduck/sentry.io/invite_member`
- Updated: 2026-11-03 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/sentry.io/invite_member`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/sentry.io/invite_member
```

## Input

- `org` (string, required): Slug of the Sentry organization, as in https://<slug>.sentry.io.
- `email` (string, required): Email address of the person to invite.
- `role` (string, optional): Organization role: member, admin, manager or owner.
- `teams` (array, optional): Slugs of the teams to add the person to. Empty for none.

## Output

- `id` (string, required)
- `role` (string | null, required)
- `email` (string, required)
- `pending` (boolean, required)
- `expired` (boolean | null, optional)

## FAQ

### What does "Invite a member to a Sentry organization" do?

Invites one person by email to a Sentry organization with a given role, optionally adding them to teams. Returns the pending member that Sentry created. Fails with a clear message when the signed-in account may not invite members or the email is already a member.

### How do I automatically invite a member to a Sentry organization on sentry.io?

Ask an AI agent connected to Reduck to run reduck/sentry.io/invite_member, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/sentry.io/invite_member

### Is there a sentry.io API to invite a member to a Sentry organization?

You do not need one. "Invite a member to a Sentry organization" drives the real sentry.io pages in a browser, so it works whether or not sentry.io offers an API for this.

### What information do I need to provide?

Required: org, email. Optional: role, teams.

### What does it return?

It returns id, role, email, expired, pending.

### Do I need to be logged in to sentry.io?

Yes. It acts as you on sentry.io: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the sentry.io cookies saved by the Reduck extension.

### Does it change anything on sentry.io, or only read data?

It makes changes on sentry.io, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/sentry.io/invite_member, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/sentry.io/invite_member

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/sentry.io/invite_member
