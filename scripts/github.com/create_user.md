# Invite user to GitHub org

Automatically invite user to GitHub org on github.com. Invite a person to a GitHub organization (org membership is invite-based, not instant). Identify the invitee by username, full name, or email (must resolve to a suggestion in GitHub's own invite search and not already be a member). Optional role: "member" (default) or "owner". Returns the confirmation banner text.

- Site: github.com
- Address: `reduck/github.com/create_user`
- Updated: 2026-08-27 (v5)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/github.com/create_user`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/github.com/create_user
```

## Input

- `org` (string, required): GitHub organization login/slug, e.g. "testeraccount-pointandclick-org".
- `identifier` (string, required)
- `role` (string, optional)

## Output

- `org` (string, required)
- `role` (string, required)
- `message` (string | null, required): The confirmation banner text shown after sending the invitation.
- `identifier` (string, required)

## FAQ

### What does "Invite user to GitHub org" do?

Invite a person to a GitHub organization (org membership is invite-based, not instant). Identify the invitee by username, full name, or email (must resolve to a suggestion in GitHub's own invite search and not already be a member). Optional role: "member" (default) or "owner". Returns the confirmation banner text.

### How do I automatically invite user to GitHub org on github.com?

Ask an AI agent connected to Reduck to run reduck/github.com/create_user, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/github.com/create_user

### Is there a github.com API to invite user to GitHub org?

You do not need one. "Invite user to GitHub org" drives the real github.com pages in a browser, so it works whether or not github.com offers an API for this.

### What information do I need to provide?

Required: org, identifier. Optional: role.

### What does it return?

It returns org, role, message, identifier.

### Do I need to be logged in to github.com?

Yes. It acts as you on github.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the github.com cookies saved by the Reduck extension.

### Does it change anything on github.com, or only read data?

It makes changes on github.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/github.com/create_user, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/github.com/create_user

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/github.com/create_user
