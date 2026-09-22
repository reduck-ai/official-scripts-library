# Cloudflare: remove member

Automatically remove member on cloudflare.com. Remove a member from one Cloudflare account by email, via the Members list's "Remove member" action. Returns the removed email, accountId and status.

- Site: cloudflare.com
- Address: `reduck/cloudflare.com/delete_user`
- Updated: 2026-07-31 (v6)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/cloudflare.com/delete_user`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/cloudflare.com/delete_user
```

## Input

- `email` (string, required): Email address of the member to remove.
- `accountId` (string, required): Cloudflare account id to remove the member from.

## Output

- `email` (string, required)
- `status` (string, required)
- `accountId` (string, required)

## FAQ

### What does "Cloudflare: remove member" do?

Remove a member from one Cloudflare account by email, via the Members list's "Remove member" action. Returns the removed email, accountId and status.

### How do I automatically remove member on cloudflare.com?

Ask an AI agent connected to Reduck to run reduck/cloudflare.com/delete_user, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/cloudflare.com/delete_user

### Is there a cloudflare.com API to remove member?

You do not need one. "Cloudflare: remove member" drives the real cloudflare.com pages in a browser, so it works whether or not cloudflare.com offers an API for this.

### What information do I need to provide?

Required: accountId, email.

### What does it return?

It returns email, status, accountId.

### Do I need to be logged in to cloudflare.com?

Yes. It acts as you on cloudflare.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the cloudflare.com cookies saved by the Reduck extension.

### Does it change anything on cloudflare.com, or only read data?

It makes changes on cloudflare.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/cloudflare.com/delete_user, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/cloudflare.com/delete_user

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/cloudflare.com/delete_user
