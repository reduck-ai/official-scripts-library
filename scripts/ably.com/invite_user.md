# Invite a user to the Ably account team

Automatically invite a user to the Ably account team on ably.com. Invites a person to the signed-in Ably account's team by name and email, with the chosen roles (admin, developer, billing). Returns the invitation as the team page then shows it, with its labels. Fails with a sign-in error when the browser is not signed in to Ably, and with the site's message when the invitation is refused (invalid email, person already invited or already a member).

- Site: ably.com
- Address: `reduck/ably.com/invite_user`
- Updated: 2026-11-26 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/ably.com/invite_user`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/ably.com/invite_user
```

## Input

- `name` (string, required): Full name of the person to invite.
- `email` (string, required): Email address the invitation is sent to.
- `roles` (array, optional): Roles given to the person. The site's default is developer only.

## Output

- `email` (string, required)
- `roles` (array, required)
- `member` (object | null, required): The row the team page shows for this email after the invitation, or null if it is not listed.
- `invited` (boolean, required)

## FAQ

### What does "Invite a user to the Ably account team" do?

Invites a person to the signed-in Ably account's team by name and email, with the chosen roles (admin, developer, billing). Returns the invitation as the team page then shows it, with its labels. Fails with a sign-in error when the browser is not signed in to Ably, and with the site's message when the invitation is refused (invalid email, person already invited or already a member).

### How do I automatically invite a user to the Ably account team on ably.com?

Ask an AI agent connected to Reduck to run reduck/ably.com/invite_user, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/ably.com/invite_user

### Is there a ably.com API to invite a user to the Ably account team?

You do not need one. "Invite a user to the Ably account team" drives the real ably.com pages in a browser, so it works whether or not ably.com offers an API for this.

### What information do I need to provide?

Required: name, email. Optional: roles.

### What does it return?

It returns email, roles, member, invited.

### Do I need to be logged in to ably.com?

Yes. It acts as you on ably.com: in your browser it reuses your session, and on a cloud browser it loads your Auth session cookies for ably.com.

### Does it change anything on ably.com, or only read data?

It makes changes on ably.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/ably.com/invite_user, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/ably.com/invite_user

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/ably.com/invite_user
