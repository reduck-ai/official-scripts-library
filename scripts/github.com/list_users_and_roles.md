# List GitHub org members and roles

Automatically list GitHub org members and roles on github.com. List a GitHub organization's members (login, org role Owner/Member, profile URL) and pending invitations (email, role). Reads the org's People and Invitations tabs. Requires org (the org login/slug).

- Site: github.com
- Address: `reduck/github.com/list_users_and_roles`
- Updated: 2026-09-07 (v11)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/github.com/list_users_and_roles`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/github.com/list_users_and_roles
```

## Input

- `org` (string, required): GitHub organization login, e.g. "acme" (from github.com/orgs/<org>/people).

## Output

- `org` (string, required)
- `members` (array, required)
- `pendingInvitations` (array, required)
- `membersNote` (string, optional)
- `pendingInvitationsNote` (string, optional)

## FAQ

### What does "List GitHub org members and roles" do?

List a GitHub organization's members (login, org role Owner/Member, profile URL) and pending invitations (email, role). Reads the org's People and Invitations tabs. Requires org (the org login/slug).

### How do I automatically list GitHub org members and roles on github.com?

Ask an AI agent connected to Reduck to run reduck/github.com/list_users_and_roles, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/github.com/list_users_and_roles

### Is there a github.com API to list GitHub org members and roles?

You do not need one. "List GitHub org members and roles" drives the real github.com pages in a browser, so it works whether or not github.com offers an API for this.

### What information do I need to provide?

Required: org.

### What does it return?

It returns org, members, membersNote, pendingInvitations, pendingInvitationsNote.

### Do I need to be logged in to github.com?

Yes. It acts as you on github.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the github.com cookies saved by the Reduck extension.

### Does it change anything on github.com, or only read data?

It only reads. It looks things up on github.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/github.com/list_users_and_roles, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/github.com/list_users_and_roles

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/github.com/list_users_and_roles
