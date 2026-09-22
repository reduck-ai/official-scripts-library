# Remove DigitalOcean team member

Automatically remove DigitalOcean team member on cloud.digitalocean.com. Remove a member, or cancel a pending invite, from the current DigitalOcean team, identified by email. Finds their row, opens its row menu, and confirms the appropriate dialog: "Remove from team" for joined members (requires re-typing their email to confirm) or "Cancel invite" for pending invites (plain yes/no). Returns the removed email.

- Site: cloud.digitalocean.com
- Address: `reduck/cloud.digitalocean.com/delete_user`
- Updated: 2026-07-31 (v4)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/cloud.digitalocean.com/delete_user`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/cloud.digitalocean.com/delete_user
```

## Input

- `email` (string, required): Email of the member or pending invite to remove.

## Output

- `email` (string, required)
- `removed` (boolean, required)

## FAQ

### What does "Remove DigitalOcean team member" do?

Remove a member, or cancel a pending invite, from the current DigitalOcean team, identified by email. Finds their row, opens its row menu, and confirms the appropriate dialog: "Remove from team" for joined members (requires re-typing their email to confirm) or "Cancel invite" for pending invites (plain yes/no). Returns the removed email.

### How do I automatically remove DigitalOcean team member on cloud.digitalocean.com?

Ask an AI agent connected to Reduck to run reduck/cloud.digitalocean.com/delete_user, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/cloud.digitalocean.com/delete_user

### Is there a cloud.digitalocean.com API to remove DigitalOcean team member?

You do not need one. "Remove DigitalOcean team member" drives the real cloud.digitalocean.com pages in a browser, so it works whether or not cloud.digitalocean.com offers an API for this.

### What information do I need to provide?

Required: email.

### What does it return?

It returns email, removed.

### Do I need to be logged in to cloud.digitalocean.com?

Yes. It acts as you on cloud.digitalocean.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the cloud.digitalocean.com cookies saved by the Reduck extension.

### Does it change anything on cloud.digitalocean.com, or only read data?

It makes changes on cloud.digitalocean.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/cloud.digitalocean.com/delete_user, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/cloud.digitalocean.com/delete_user

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/cloud.digitalocean.com/delete_user
