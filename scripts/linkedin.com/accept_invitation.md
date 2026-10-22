# LinkedIn — accept a received invitation

Automatically accept a received invitation on linkedin.com. Accept a pending received LinkedIn invitation, by its invitation id from get_received_invitations (preferred) or by the inviter's display name. A name that matches two invitations throws rather than guess, and a name that is only in "Suggestions for you" gets a clear error (there is nothing to accept). dryRun finds and checks the invitation without accepting it. Returns the status and the matched card text so you can confirm the right one was accepted.

- Site: linkedin.com
- Address: `reduck/linkedin.com/accept_invitation`
- Updated: 2026-10-21 (v6)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/linkedin.com/accept_invitation`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/linkedin.com/accept_invitation
```

## Input

- `name` (string, optional): Inviter's display name exactly as shown on the invitation (e.g. "Ossama Messaoudi", or a page name like "Marketer Tips"), when you have no invitationUrn. Two or more matching invitations throw.
- `dryRun` (boolean, optional): Find and check the invitation, but do not click Accept. Returns status "dry_run".
- `invitationUrn` (string, optional): The invitation's urn:li:invitation:<id>, as get_received_invitations returns it. Preferred: it targets one row exactly.

## Output

- `status` (string, required): "accepted" when the invitation left the pending list; "dry_run" when dryRun stopped before the click.
- `name` (string | null, optional): Echo of the requested name, or null when targeted by invitationUrn.
- `invitationUrn` (string | null, optional): urn:li:invitation:<id> of the matched row.
- `recipientResolved` (string | null, optional): Trimmed text of the matched invitation card — cross-check the right person/page was accepted.

## FAQ

### What does "LinkedIn — accept a received invitation" do?

Accept a pending received LinkedIn invitation, by its invitation id from get_received_invitations (preferred) or by the inviter's display name. A name that matches two invitations throws rather than guess, and a name that is only in "Suggestions for you" gets a clear error (there is nothing to accept). dryRun finds and checks the invitation without accepting it. Returns the status and the matched card text so you can confirm the right one was accepted.

### How do I automatically accept a received invitation on linkedin.com?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/accept_invitation, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/accept_invitation

### Is there a linkedin.com API to accept a received invitation?

You do not need one. "LinkedIn — accept a received invitation" drives the real linkedin.com pages in a browser, so it works whether or not linkedin.com offers an API for this.

### What information do I need to provide?

Optional: name, dryRun, invitationUrn.

### What does it return?

It returns name, status, invitationUrn, recipientResolved.

### Do I need to be logged in to linkedin.com?

Yes. It acts as you on linkedin.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the linkedin.com cookies saved by the Reduck extension.

### Does it change anything on linkedin.com, or only read data?

It makes changes on linkedin.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/accept_invitation, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/accept_invitation

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/linkedin.com/accept_invitation
