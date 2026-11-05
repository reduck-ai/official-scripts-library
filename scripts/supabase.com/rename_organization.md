# Rename Supabase Organization

Automatically rename Supabase Organization on supabase.com. Renames a Supabase organization, identified by its slug, to a new display name. The slug itself does not change. Returns the name before and after as the dashboard stores them. Requires being signed in as a member allowed to edit the organization, and fails with a clear message when the signed-in account cannot edit it or the new name is empty.

- Site: supabase.com
- Address: `reduck/supabase.com/rename_organization`
- Updated: 2026-11-04 (v4)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/supabase.com/rename_organization`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/supabase.com/rename_organization
```

## Input

- `name` (string, required): New display name for the organization.
- `orgId` (string, required): Organization slug, e.g. "czohueidxubssokhivlp" (from supabase.com/list_users_and_roles, orgSlug field).

## Output

- `name` (string, required)
- `orgId` (string, required)
- `previousName` (string, required)

## FAQ

### What does "Rename Supabase Organization" do?

Renames a Supabase organization, identified by its slug, to a new display name. The slug itself does not change. Returns the name before and after as the dashboard stores them. Requires being signed in as a member allowed to edit the organization, and fails with a clear message when the signed-in account cannot edit it or the new name is empty.

### How do I automatically rename Supabase Organization on supabase.com?

Ask an AI agent connected to Reduck to run reduck/supabase.com/rename_organization, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/supabase.com/rename_organization

### Is there a supabase.com API to rename Supabase Organization?

You do not need one. "Rename Supabase Organization" drives the real supabase.com pages in a browser, so it works whether or not supabase.com offers an API for this.

### What information do I need to provide?

Required: orgId, name.

### What does it return?

It returns name, orgId, previousName.

### Do I need to be logged in to supabase.com?

Yes. It acts as you on supabase.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the supabase.com cookies saved by the Reduck extension.

### Does it change anything on supabase.com, or only read data?

It makes changes on supabase.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/supabase.com/rename_organization, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/supabase.com/rename_organization

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/supabase.com/rename_organization
