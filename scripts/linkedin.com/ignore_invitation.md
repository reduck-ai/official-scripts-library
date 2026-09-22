# LinkedIn — ignore a received invitation

Automatically ignore a received invitation on linkedin.com. Ignore (decline) a pending received invitation on LinkedIn, identified by the inviter's display name (person or page). Guards against homonyms - two or more pending matches throw rather than guess - and returns the status plus the matched name (recipientResolved). Only acts on invitations already loaded, and is not easily reversible.

- Site: linkedin.com
- Address: `reduck/linkedin.com/ignore_invitation`
- Updated: 2026-08-07 (v4)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/linkedin.com/ignore_invitation`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/linkedin.com/ignore_invitation
```

## Input

- `name` (string, required): Inviter's display name exactly as shown on the invitation. The pending invitation matching this name is ignored; ambiguous (multiple) matches throw.

## Output

- `name` (string, required): Echo of the requested name.
- `status` (string, required): "ignored" when the invitation left the pending list.
- `recipientResolved` (string | null, optional): Trimmed text of the matched invitation card — cross-check the right person/page was ignored.

## FAQ

### What does "LinkedIn — ignore a received invitation" do?

Ignore (decline) a pending received invitation on LinkedIn, identified by the inviter's display name (person or page). Guards against homonyms - two or more pending matches throw rather than guess - and returns the status plus the matched name (recipientResolved). Only acts on invitations already loaded, and is not easily reversible.

### How do I automatically ignore a received invitation on linkedin.com?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/ignore_invitation, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/ignore_invitation

### Is there a linkedin.com API to ignore a received invitation?

You do not need one. "LinkedIn — ignore a received invitation" drives the real linkedin.com pages in a browser, so it works whether or not linkedin.com offers an API for this.

### What information do I need to provide?

Required: name.

### What does it return?

It returns name, status, recipientResolved.

### Do I need to be logged in to linkedin.com?

Yes. It acts as you on linkedin.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the linkedin.com cookies saved by the Reduck extension.

### Does it change anything on linkedin.com, or only read data?

It makes changes on linkedin.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/ignore_invitation, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/ignore_invitation

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/linkedin.com/ignore_invitation
