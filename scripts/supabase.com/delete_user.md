# Remove Team Member

Automatically remove Team Member on supabase.com. Removes a member from a Supabase organization by email — revokes membership for an active member, or cancels their invite if they're only a pending invitee. Returns their prior status and confirmation of removal.

- Site: supabase.com
- Address: `reduck/supabase.com/delete_user`
- Updated: 2026-07-31 (v4)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/supabase.com/delete_user`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/supabase.com/delete_user
```

## Input

- `email` (string, required): Email of the member or pending invitee to remove.
- `orgId` (string, required): Organization slug, e.g. "czohueidxubssokhivlp" (from list_users_and_roles' orgSlug field).

## Output

- `email` (string, required)
- `orgId` (string, required)
- `status` (string, required)
- `previousStatus` (string, required)

## FAQ

### What does "Remove Team Member" do?

Removes a member from a Supabase organization by email — revokes membership for an active member, or cancels their invite if they're only a pending invitee. Returns their prior status and confirmation of removal.

### How do I automatically remove Team Member on supabase.com?

Ask an AI agent connected to Reduck to run reduck/supabase.com/delete_user, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/supabase.com/delete_user

### Is there a supabase.com API to remove Team Member?

You do not need one. "Remove Team Member" drives the real supabase.com pages in a browser, so it works whether or not supabase.com offers an API for this.

### What information do I need to provide?

Required: orgId, email.

### What does it return?

It returns email, orgId, status, previousStatus.

### Do I need to be logged in to supabase.com?

Yes. It acts as you on supabase.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the supabase.com cookies saved by the Reduck extension.

### Does it change anything on supabase.com, or only read data?

It makes changes on supabase.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/supabase.com/delete_user, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/supabase.com/delete_user

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/supabase.com/delete_user
