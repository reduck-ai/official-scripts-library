# List DigitalOcean team members and roles

Automatically list DigitalOcean team members and roles on cloud.digitalocean.com. List the current DigitalOcean team's members and pending invites with their role, status (Joined/Pending) and sign-in method. No scoping arg — reads the signed-in team, matching list_invoices' convention for this host.

- Site: cloud.digitalocean.com
- Address: `reduck/cloud.digitalocean.com/list_users_and_roles`
- Updated: 2026-07-29 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/cloud.digitalocean.com/list_users_and_roles`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/cloud.digitalocean.com/list_users_and_roles
```

## Input

It takes no input.

## Output

- `count` (integer, required)
- `members` (array, required)

## FAQ

### What does "List DigitalOcean team members and roles" do?

List the current DigitalOcean team's members and pending invites with their role, status (Joined/Pending) and sign-in method. No scoping arg — reads the signed-in team, matching list_invoices' convention for this host.

### How do I automatically list DigitalOcean team members and roles on cloud.digitalocean.com?

Ask an AI agent connected to Reduck to run reduck/cloud.digitalocean.com/list_users_and_roles, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/cloud.digitalocean.com/list_users_and_roles

### Is there a cloud.digitalocean.com API to list DigitalOcean team members and roles?

You do not need one. "List DigitalOcean team members and roles" drives the real cloud.digitalocean.com pages in a browser, so it works whether or not cloud.digitalocean.com offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns count, members.

### Do I need to be logged in to cloud.digitalocean.com?

Yes. It acts as you on cloud.digitalocean.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the cloud.digitalocean.com cookies saved by the Reduck extension.

### Does it change anything on cloud.digitalocean.com, or only read data?

Unknown: its author has not declared whether it changes anything on cloud.digitalocean.com, so treat it as if it could.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/cloud.digitalocean.com/list_users_and_roles, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/cloud.digitalocean.com/list_users_and_roles

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/cloud.digitalocean.com/list_users_and_roles
