# List GitHub org members and roles

Automatically list GitHub org members and roles on github.com. List a GitHub organization's members (login, profile URL, and org role when the account can see it), one page of 30 at a time, with hasNextPage and totalPages for paging, plus pending invitations (email, role), which only org owners can see; otherwise the list is empty with a note saying why. Requires org (the org login). Fails with a sign-in error when the browser is not signed in to GitHub.

- Site: github.com
- Address: `reduck/github.com/list_users_and_roles`
- Updated: 2026-10-23 (v13)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/github.com/list_users_and_roles`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/github.com/list_users_and_roles
```

## Input

- `org` (string, required): GitHub organization login, e.g. "acme" (from github.com/orgs/<org>/people).
- `page` (integer, optional): Page of the members list, 1-indexed (GitHub shows 30 people per page). Use hasNextPage to know whether to ask for the next one.

## Output

- `org` (string, required)
- `page` (integer, required)
- `members` (array, required)
- `hasNextPage` (boolean, required)
- `pendingInvitations` (array, required)
- `totalPages` (integer | null, optional)
- `membersNote` (string, optional)
- `pendingInvitationsNote` (string, optional)

## FAQ

### What does "List GitHub org members and roles" do?

List a GitHub organization's members (login, profile URL, and org role when the account can see it), one page of 30 at a time, with hasNextPage and totalPages for paging, plus pending invitations (email, role), which only org owners can see; otherwise the list is empty with a note saying why. Requires org (the org login). Fails with a sign-in error when the browser is not signed in to GitHub.

### How do I automatically list GitHub org members and roles on github.com?

Ask an AI agent connected to Reduck to run reduck/github.com/list_users_and_roles, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/github.com/list_users_and_roles

### Is there a github.com API to list GitHub org members and roles?

You do not need one. "List GitHub org members and roles" drives the real github.com pages in a browser, so it works whether or not github.com offers an API for this.

### What information do I need to provide?

Required: org. Optional: page.

### What does it return?

It returns org, page, members, totalPages, hasNextPage, membersNote, pendingInvitations, pendingInvitationsNote.

### Do I need to be logged in to github.com?

Yes. It acts as you on github.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the github.com cookies saved by the Reduck extension.

### Does it change anything on github.com, or only read data?

It only reads. It looks things up on github.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/github.com/list_users_and_roles, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/github.com/list_users_and_roles

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/github.com/list_users_and_roles
