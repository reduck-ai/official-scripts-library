# Remove Neon organization member

Automatically remove Neon organization member on console.neon.tech. Remove a member, or cancel a pending invite, from the current Neon organization, identified by email. Checks the org's members and invitations lists to determine which branch applies: joined members are removed via "Remove from organization" (plain confirm, no re-typing required); pending invites are cancelled via "Cancel invite". Returns the removed email and whether it was a pending invite.

- Site: console.neon.tech
- Address: `reduck/console.neon.tech/delete_user`
- Updated: 2026-08-27 (v5)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/console.neon.tech/delete_user`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/console.neon.tech/delete_user
```

## Input

- `email` (string, required): Email of the member or pending invite to remove.

## Output

- `email` (string, required)
- `removed` (boolean, required)
- `wasPending` (boolean, required)

## FAQ

### What does "Remove Neon organization member" do?

Remove a member, or cancel a pending invite, from the current Neon organization, identified by email. Checks the org's members and invitations lists to determine which branch applies: joined members are removed via "Remove from organization" (plain confirm, no re-typing required); pending invites are cancelled via "Cancel invite". Returns the removed email and whether it was a pending invite.

### How do I automatically remove Neon organization member on console.neon.tech?

Ask an AI agent connected to Reduck to run reduck/console.neon.tech/delete_user, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/console.neon.tech/delete_user

### Is there a console.neon.tech API to remove Neon organization member?

You do not need one. "Remove Neon organization member" drives the real console.neon.tech pages in a browser, so it works whether or not console.neon.tech offers an API for this.

### What information do I need to provide?

Required: email.

### What does it return?

It returns email, removed, wasPending.

### Do I need to be logged in to console.neon.tech?

Yes. It acts as you on console.neon.tech: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the console.neon.tech cookies saved by the Reduck extension.

### Does it change anything on console.neon.tech, or only read data?

It makes changes on console.neon.tech, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/console.neon.tech/delete_user, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/console.neon.tech/delete_user

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/console.neon.tech/delete_user
