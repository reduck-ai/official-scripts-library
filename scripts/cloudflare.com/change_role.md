# Cloudflare: change member role

Automatically change member role on cloudflare.com. Change one member's role within one Cloudflare account: looks up the member by email via the account's members API, opens their single account-wide permission policy, toggles off their current role(s) and toggles on the named new role (matched against the account's own role picker), then saves. Throws if the member has anything other than exactly one permission policy (ambiguous case, not handled). Returns previous and new roles.

- Site: cloudflare.com
- Address: `reduck/cloudflare.com/change_role`
- Updated: 2026-07-31 (v5)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/cloudflare.com/change_role`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/cloudflare.com/change_role
```

## Input

- `role` (string, required): Exact new role name as shown in the account's permission-policy role picker, e.g. "Administrator", "Billing".
- `email` (string, required): Email address of the member to change.
- `accountId` (string, required): Cloudflare account id the member belongs to.

## Output

- `email` (string, required)
- `newRole` (string, required)
- `accountId` (string, required)
- `previousRoles` (array, required)

## FAQ

### What does "Cloudflare: change member role" do?

Change one member's role within one Cloudflare account: looks up the member by email via the account's members API, opens their single account-wide permission policy, toggles off their current role(s) and toggles on the named new role (matched against the account's own role picker), then saves. Throws if the member has anything other than exactly one permission policy (ambiguous case, not handled). Returns previous and new roles.

### How do I automatically change member role on cloudflare.com?

Ask an AI agent connected to Reduck to run reduck/cloudflare.com/change_role, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/cloudflare.com/change_role

### Is there a cloudflare.com API to change member role?

You do not need one. "Cloudflare: change member role" drives the real cloudflare.com pages in a browser, so it works whether or not cloudflare.com offers an API for this.

### What information do I need to provide?

Required: accountId, email, role.

### What does it return?

It returns email, newRole, accountId, previousRoles.

### Do I need to be logged in to cloudflare.com?

Yes. It acts as you on cloudflare.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the cloudflare.com cookies saved by the Reduck extension.

### Does it change anything on cloudflare.com, or only read data?

It makes changes on cloudflare.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/cloudflare.com/change_role, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/cloudflare.com/change_role

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/cloudflare.com/change_role
