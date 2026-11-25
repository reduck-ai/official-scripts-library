# Invite Neon organization member

Automatically invite Neon organization member on console.neon.tech. Invite a member to the current Neon organization by email with one of Neon's organization roles. The invitee shows as Pending until they accept (someone who already has a Neon account may join directly). Returns the invitation's email, role, id and invited-at time.

- Site: console.neon.tech
- Address: `reduck/console.neon.tech/create_user`
- Updated: 2026-11-24 (v10)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/console.neon.tech/create_user`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/console.neon.tech/create_user
```

## Input

- `role` (string, required): Org role to invite them with. "Member" is Neon's own role name for what its UI currently displays as "Editor" — pass the role name, not the UI label; both are accepted case-insensitively.
- `email` (string, required): Email address to invite.

## Output

- `role` (string, required)
- `email` (string, required)
- `invitationId` (string, required)
- `invitedAt` (string | null, optional)

## FAQ

### What does "Invite Neon organization member" do?

Invite a member to the current Neon organization by email with one of Neon's organization roles. The invitee shows as Pending until they accept (someone who already has a Neon account may join directly). Returns the invitation's email, role, id and invited-at time.

### How do I automatically invite Neon organization member on console.neon.tech?

Ask an AI agent connected to Reduck to run reduck/console.neon.tech/create_user, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/console.neon.tech/create_user

### Is there a console.neon.tech API to invite Neon organization member?

You do not need one. "Invite Neon organization member" drives the real console.neon.tech pages in a browser, so it works whether or not console.neon.tech offers an API for this.

### What information do I need to provide?

Required: email, role.

### What does it return?

It returns role, email, invitedAt, invitationId.

### Do I need to be logged in to console.neon.tech?

Yes. It acts as you on console.neon.tech: in your browser it reuses your session, and on a cloud browser it loads your Auth session cookies for console.neon.tech.

### Does it change anything on console.neon.tech, or only read data?

It makes changes on console.neon.tech, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/console.neon.tech/create_user, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/console.neon.tech/create_user

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/console.neon.tech/create_user
