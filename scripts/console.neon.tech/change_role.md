# Change Neon organization member's role

Automatically change Neon organization member's role on console.neon.tech. Change a joined member's role on the current Neon organization, identified by email. The role (Admin or Member) is matched case-insensitively. Only applies to members who have joined: a pending invite's role is set at invite time, so cancel and re-invite to change it. If the member already has the requested role, nothing changes and changed is false. Returns the member's email, resulting role, and whether a change occurred.

- Site: console.neon.tech
- Address: `reduck/console.neon.tech/change_role`
- Updated: 2026-10-23 (v6)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/console.neon.tech/change_role`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/console.neon.tech/change_role
```

## Input

- `role` (string, required): New role name as shown in Neon's People page role menu: Admin or Member. Case-insensitive match.
- `email` (string, required): Email of the joined organization member whose role to change.

## Output

- `role` (string, required)
- `email` (string, required)
- `changed` (boolean, required)

## FAQ

### What does "Change Neon organization member's role" do?

Change a joined member's role on the current Neon organization, identified by email. The role (Admin or Member) is matched case-insensitively. Only applies to members who have joined: a pending invite's role is set at invite time, so cancel and re-invite to change it. If the member already has the requested role, nothing changes and changed is false. Returns the member's email, resulting role, and whether a change occurred.

### How do I automatically change Neon organization member's role on console.neon.tech?

Ask an AI agent connected to Reduck to run reduck/console.neon.tech/change_role, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/console.neon.tech/change_role

### Is there a console.neon.tech API to change Neon organization member's role?

You do not need one. "Change Neon organization member's role" drives the real console.neon.tech pages in a browser, so it works whether or not console.neon.tech offers an API for this.

### What information do I need to provide?

Required: email, role.

### What does it return?

It returns role, email, changed.

### Do I need to be logged in to console.neon.tech?

Yes. It acts as you on console.neon.tech: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the console.neon.tech cookies saved by the Reduck extension.

### Does it change anything on console.neon.tech, or only read data?

It makes changes on console.neon.tech, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/console.neon.tech/change_role, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/console.neon.tech/change_role

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/console.neon.tech/change_role
