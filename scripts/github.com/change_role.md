# Change GitHub org member's role

Automatically change GitHub org member's role on github.com. Change an existing GitHub org member's role between Member and Owner (via People > row menu > Change role). Identify the member by their GitHub username/login (not their invite email — this only works on accepted members, not pending invitations). Returns the confirmation banner text.

- Site: github.com
- Address: `reduck/github.com/change_role`
- Updated: 2026-08-27 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/github.com/change_role`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/github.com/change_role
```

## Input

- `org` (string, required)
- `role` (string, required)
- `username` (string, required)

## Output

- `org` (string, required)
- `role` (string, required)
- `username` (string, required)
- `message` (string | null, optional)

## FAQ

### What does "Change GitHub org member's role" do?

Change an existing GitHub org member's role between Member and Owner (via People > row menu > Change role). Identify the member by their GitHub username/login (not their invite email — this only works on accepted members, not pending invitations). Returns the confirmation banner text.

### How do I automatically change GitHub org member's role on github.com?

Ask an AI agent connected to Reduck to run reduck/github.com/change_role, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/github.com/change_role

### Is there a github.com API to change GitHub org member's role?

You do not need one. "Change GitHub org member's role" drives the real github.com pages in a browser, so it works whether or not github.com offers an API for this.

### What information do I need to provide?

Required: org, username, role.

### What does it return?

It returns org, role, message, username.

### Do I need to be logged in to github.com?

Yes. It acts as you on github.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the github.com cookies saved by the Reduck extension.

### Does it change anything on github.com, or only read data?

It makes changes on github.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/github.com/change_role, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/github.com/change_role

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/github.com/change_role
