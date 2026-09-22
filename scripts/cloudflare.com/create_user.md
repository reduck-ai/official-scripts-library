# Cloudflare: invite member

Automatically invite member on cloudflare.com. Invite a new member into one Cloudflare account by email, granting an account-wide permission policy for a named role (e.g. "Administrator", "Billing") matched against the account's own role picker. Returns the invited email, role, accountId and pending status.

- Site: cloudflare.com
- Address: `reduck/cloudflare.com/create_user`
- Updated: 2026-07-31 (v5)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/cloudflare.com/create_user`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/cloudflare.com/create_user
```

## Input

- `role` (string, required): Exact role name as shown in the account's permission-policy role picker, e.g. "Administrator", "Billing", "Super Administrator - All Privileges".
- `email` (string, required): Email address to invite.
- `accountId` (string, required): Cloudflare account id to invite into (from the dash.cloudflare.com/<accountId>/... URL).

## Output

- `role` (string, required)
- `email` (string, required)
- `status` (string, required)
- `accountId` (string, required)

## FAQ

### What does "Cloudflare: invite member" do?

Invite a new member into one Cloudflare account by email, granting an account-wide permission policy for a named role (e.g. "Administrator", "Billing") matched against the account's own role picker. Returns the invited email, role, accountId and pending status.

### How do I automatically invite member on cloudflare.com?

Ask an AI agent connected to Reduck to run reduck/cloudflare.com/create_user, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/cloudflare.com/create_user

### Is there a cloudflare.com API to invite member?

You do not need one. "Cloudflare: invite member" drives the real cloudflare.com pages in a browser, so it works whether or not cloudflare.com offers an API for this.

### What information do I need to provide?

Required: accountId, email, role.

### What does it return?

It returns role, email, status, accountId.

### Do I need to be logged in to cloudflare.com?

Yes. It acts as you on cloudflare.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the cloudflare.com cookies saved by the Reduck extension.

### Does it change anything on cloudflare.com, or only read data?

It makes changes on cloudflare.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/cloudflare.com/create_user, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/cloudflare.com/create_user

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/cloudflare.com/create_user
