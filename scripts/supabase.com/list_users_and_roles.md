# List Team Members and Roles

Automatically list Team Members and Roles on supabase.com. Lists every organization the current Supabase account belongs to, with each org's active members (email, username, role, MFA status) and pending invitations (email, role, invited-at). No scoping argument — loops every visible organization, mirroring the existing list_invoices convention for this host.

- Site: supabase.com
- Address: `reduck/supabase.com/list_users_and_roles`
- Updated: 2026-07-27 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/supabase.com/list_users_and_roles`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/supabase.com/list_users_and_roles
```

## Input

It takes no input.

## FAQ

### What does "List Team Members and Roles" do?

Lists every organization the current Supabase account belongs to, with each org's active members (email, username, role, MFA status) and pending invitations (email, role, invited-at). No scoping argument — loops every visible organization, mirroring the existing list_invoices convention for this host.

### How do I automatically list Team Members and Roles on supabase.com?

Ask an AI agent connected to Reduck to run reduck/supabase.com/list_users_and_roles, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/supabase.com/list_users_and_roles

### Is there a supabase.com API to list Team Members and Roles?

You do not need one. "List Team Members and Roles" drives the real supabase.com pages in a browser, so it works whether or not supabase.com offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### Do I need to be logged in to supabase.com?

Yes. It acts as you on supabase.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the supabase.com cookies saved by the Reduck extension.

### Does it change anything on supabase.com, or only read data?

Unknown: its author has not declared whether it changes anything on supabase.com, so treat it as if it could.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/supabase.com/list_users_and_roles, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/supabase.com/list_users_and_roles

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/supabase.com/list_users_and_roles
