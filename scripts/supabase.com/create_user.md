# Invite Team Member

Automatically invite Team Member on supabase.com. Invites a new member to a Supabase organization by email with a given role (matched against the org's own role picker, e.g. Owner/Administrator/Developer). Supabase org membership is invite-based, so this sends an invitation rather than creating an active member directly. Returns the invited email, matched role, and pending status.

- Site: supabase.com
- Address: `reduck/supabase.com/create_user`
- Updated: 2026-07-31 (v6)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/supabase.com/create_user`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/supabase.com/create_user
```

## Input

- `role` (string, required): Role name matched against the organization's own role picker (e.g. "Owner", "Administrator", "Developer"). Case-insensitive.
- `email` (string, required): Email address to invite.
- `orgId` (string, required): Organization slug, e.g. "czohueidxubssokhivlp" (from list_users_and_roles' orgSlug field).

## Output

- `role` (string, required)
- `email` (string, required)
- `orgId` (string, required)
- `status` (string, required)
- `invitedAt` (string, required)

## FAQ

### What does "Invite Team Member" do?

Invites a new member to a Supabase organization by email with a given role (matched against the org's own role picker, e.g. Owner/Administrator/Developer). Supabase org membership is invite-based, so this sends an invitation rather than creating an active member directly. Returns the invited email, matched role, and pending status.

### How do I automatically invite Team Member on supabase.com?

Ask an AI agent connected to Reduck to run reduck/supabase.com/create_user, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/supabase.com/create_user

### Is there a supabase.com API to invite Team Member?

You do not need one. "Invite Team Member" drives the real supabase.com pages in a browser, so it works whether or not supabase.com offers an API for this.

### What information do I need to provide?

Required: orgId, email, role.

### What does it return?

It returns role, email, orgId, status, invitedAt.

### Do I need to be logged in to supabase.com?

Yes. It acts as you on supabase.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the supabase.com cookies saved by the Reduck extension.

### Does it change anything on supabase.com, or only read data?

It makes changes on supabase.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/supabase.com/create_user, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/supabase.com/create_user

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/supabase.com/create_user
