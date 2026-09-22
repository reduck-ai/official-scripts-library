# Remove user from GitHub org

Automatically remove user from GitHub org on github.com. Remove a person from a GitHub organization. If they're an accepted member, identify by GitHub username and this removes their org membership. If they're still a pending invitation, identify by the email/username they were invited with and this cancels the invitation instead. Returns which case applied and the confirmation banner text.

- Site: github.com
- Address: `reduck/github.com/delete_user`
- Updated: 2026-08-27 (v5)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/github.com/delete_user`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/github.com/delete_user
```

## Input

- `org` (string, required): GitHub organization login/slug, e.g. "testeraccount-pointandclick-org".
- `identifier` (string, required): The member's GitHub username (for accepted members) or the email/identifier they were invited with (for pending invitations).

## Output

- `org` (string, required)
- `message` (string | null, required): The confirmation banner text.
- `identifier` (string, required)
- `removedFrom` (string, required)

## FAQ

### What does "Remove user from GitHub org" do?

Remove a person from a GitHub organization. If they're an accepted member, identify by GitHub username and this removes their org membership. If they're still a pending invitation, identify by the email/username they were invited with and this cancels the invitation instead. Returns which case applied and the confirmation banner text.

### How do I automatically remove user from GitHub org on github.com?

Ask an AI agent connected to Reduck to run reduck/github.com/delete_user, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/github.com/delete_user

### Is there a github.com API to remove user from GitHub org?

You do not need one. "Remove user from GitHub org" drives the real github.com pages in a browser, so it works whether or not github.com offers an API for this.

### What information do I need to provide?

Required: org, identifier.

### What does it return?

It returns org, message, identifier, removedFrom.

### Do I need to be logged in to github.com?

Yes. It acts as you on github.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the github.com cookies saved by the Reduck extension.

### Does it change anything on github.com, or only read data?

It makes changes on github.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/github.com/delete_user, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/github.com/delete_user

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/github.com/delete_user
