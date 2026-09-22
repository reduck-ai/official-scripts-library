# Invite DigitalOcean team member

Automatically invite DigitalOcean team member on cloud.digitalocean.com. Invite (create) a member on the current DigitalOcean team by email and role. Role is free-text matched against the team's basic roles (Owner, Member, Modifier, Biller, Billing Viewer, Resource Viewer) or a custom role name if the team has any. Owner cannot be assigned directly on invite, because DigitalOcean only allows promoting to Owner after the invitee joins as a non-Owner. Returns the invited email and requested role; the member starts as Pending until they accept.

- Site: cloud.digitalocean.com
- Address: `reduck/cloud.digitalocean.com/create_user`
- Updated: 2026-08-26 (v7)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/cloud.digitalocean.com/create_user`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/cloud.digitalocean.com/create_user
```

## Input

- `role` (string, required): Role name as shown in DigitalOcean's role picker, e.g. Member, Modifier, Biller, Billing Viewer, Resource Viewer (or a custom role name). Case-sensitive match against the picker's option labels.
- `email` (string, required): Email address to invite.
- `requireSecureSignIn` (boolean, optional): Require Google/GitHub/2FA-protected sign-in for this invite. Default false (unchecked, matching the form's default).

## Output

- `role` (string, required)
- `email` (string, required)
- `invited` (boolean, required)

## FAQ

### What does "Invite DigitalOcean team member" do?

Invite (create) a member on the current DigitalOcean team by email and role. Role is free-text matched against the team's basic roles (Owner, Member, Modifier, Biller, Billing Viewer, Resource Viewer) or a custom role name if the team has any. Owner cannot be assigned directly on invite, because DigitalOcean only allows promoting to Owner after the invitee joins as a non-Owner. Returns the invited email and requested role; the member starts as Pending until they accept.

### How do I automatically invite DigitalOcean team member on cloud.digitalocean.com?

Ask an AI agent connected to Reduck to run reduck/cloud.digitalocean.com/create_user, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/cloud.digitalocean.com/create_user

### Is there a cloud.digitalocean.com API to invite DigitalOcean team member?

You do not need one. "Invite DigitalOcean team member" drives the real cloud.digitalocean.com pages in a browser, so it works whether or not cloud.digitalocean.com offers an API for this.

### What information do I need to provide?

Required: email, role. Optional: requireSecureSignIn.

### What does it return?

It returns role, email, invited.

### Do I need to be logged in to cloud.digitalocean.com?

Yes. It acts as you on cloud.digitalocean.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the cloud.digitalocean.com cookies saved by the Reduck extension.

### Does it change anything on cloud.digitalocean.com, or only read data?

It makes changes on cloud.digitalocean.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/cloud.digitalocean.com/create_user, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/cloud.digitalocean.com/create_user

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/cloud.digitalocean.com/create_user
