# Change Team Member Role

Automatically change Team Member Role on supabase.com. Changes an existing active member's role in a Supabase organization, identified by email. Matches the requested role against the org's own role picker (e.g. Owner/Administrator/Developer). Only works on already-active members — a pending invitee's role must be set at invite time (create_user) since Supabase disables role editing until the invite is accepted. Returns the role before and after the change.

- Site: supabase.com
- Address: `reduck/supabase.com/change_role`
- Updated: 2026-07-31 (v5)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/supabase.com/change_role`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/supabase.com/change_role
```

## Input

- `role` (string, required): New role name matched against the organization's own role picker (e.g. "Owner", "Administrator", "Developer"). Case-insensitive.
- `email` (string, required): Email of the active member whose role should change.
- `orgId` (string, required): Organization slug, e.g. "czohueidxubssokhivlp" (from list_users_and_roles' orgSlug field).

## Output

- `email` (string, required)
- `orgId` (string, required)
- `roleAfter` (string, required)
- `roleBefore` (string, required)

## FAQ

### What does "Change Team Member Role" do?

Changes an existing active member's role in a Supabase organization, identified by email. Matches the requested role against the org's own role picker (e.g. Owner/Administrator/Developer). Only works on already-active members — a pending invitee's role must be set at invite time (create_user) since Supabase disables role editing until the invite is accepted. Returns the role before and after the change.

### How do I automatically change Team Member Role on supabase.com?

Ask an AI agent connected to Reduck to run reduck/supabase.com/change_role, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/supabase.com/change_role

### Is there a supabase.com API to change Team Member Role?

You do not need one. "Change Team Member Role" drives the real supabase.com pages in a browser, so it works whether or not supabase.com offers an API for this.

### What information do I need to provide?

Required: orgId, email, role.

### What does it return?

It returns email, orgId, roleAfter, roleBefore.

### Do I need to be logged in to supabase.com?

Yes. It acts as you on supabase.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the supabase.com cookies saved by the Reduck extension.

### Does it change anything on supabase.com, or only read data?

It makes changes on supabase.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/supabase.com/change_role, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/supabase.com/change_role

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/supabase.com/change_role
