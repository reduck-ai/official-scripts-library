# LinkedIn — accept a received invitation

Automatically accept a received invitation on linkedin.com. Accept a pending received invitation on LinkedIn, identified by the inviter's display name (person or page). Guards against homonyms - if two or more pending invitations match the name it throws rather than guess - and returns the status plus the matched name (recipientResolved) so you can confirm the right one was accepted. Only acts on invitations already loaded in the list.

- Site: linkedin.com
- Address: `reduck/linkedin.com/accept_invitation`
- Updated: 2026-07-31 (v4)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/linkedin.com/accept_invitation`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/linkedin.com/accept_invitation
```

## Input

- `name` (string, required): Inviter's display name exactly as shown on the invitation (e.g. "Ossama Messaoudi", or a page name like "EDH Technology"). The pending invitation matching this name is accepted; ambiguous (multiple) matches throw.

## Output

- `name` (string, required): Echo of the requested name.
- `status` (string, required): "accepted" when the invitation left the pending list.
- `recipientResolved` (string | null, optional): Trimmed text of the matched invitation card — cross-check the right person/page was accepted.

## FAQ

### What does "LinkedIn — accept a received invitation" do?

Accept a pending received invitation on LinkedIn, identified by the inviter's display name (person or page). Guards against homonyms - if two or more pending invitations match the name it throws rather than guess - and returns the status plus the matched name (recipientResolved) so you can confirm the right one was accepted. Only acts on invitations already loaded in the list.

### How do I automatically accept a received invitation on linkedin.com?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/accept_invitation, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/accept_invitation

### Is there a linkedin.com API to accept a received invitation?

You do not need one. "LinkedIn — accept a received invitation" drives the real linkedin.com pages in a browser, so it works whether or not linkedin.com offers an API for this.

### What information do I need to provide?

Required: name.

### What does it return?

It returns name, status, recipientResolved.

### Do I need to be logged in to linkedin.com?

Yes. It acts as you on linkedin.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the linkedin.com cookies saved by the Reduck extension.

### Does it change anything on linkedin.com, or only read data?

It makes changes on linkedin.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/accept_invitation, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/accept_invitation

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/linkedin.com/accept_invitation
