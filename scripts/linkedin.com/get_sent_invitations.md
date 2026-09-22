# Get sent LinkedIn connection invitations

Automatically get sent LinkedIn connection invitations on linkedin.com. Lists the logged-in LinkedIn user's pending sent connection invitations (Manage invitations - Sent), and returns an empty list when there are none. Loads every invitation, with an optional limit arg to cap the count. Returns each invitee's name, headline, profile URL, personal note (if one was included), and how long ago the invite was sent.

- Site: linkedin.com
- Address: `reduck/linkedin.com/get_sent_invitations`
- Updated: 2026-09-03 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/linkedin.com/get_sent_invitations`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/linkedin.com/get_sent_invitations
```

## Input

- `limit` (number, optional): Max invitations to load by scrolling (default 100). The invitation manager lazy-loads a handful of cards at a time; the script keeps wheel-scrolling the list until this many are loaded or the list is exhausted. Set lower to cap work when you only need the top of the pile.

## Output

- `total` (number, required): Number of sent invitations returned. 0 when there are none pending.
- `invitations` (array, required)

## FAQ

### What does "Get sent LinkedIn connection invitations" do?

Lists the logged-in LinkedIn user's pending sent connection invitations (Manage invitations - Sent), and returns an empty list when there are none. Loads every invitation, with an optional limit arg to cap the count. Returns each invitee's name, headline, profile URL, personal note (if one was included), and how long ago the invite was sent.

### How do I automatically get sent LinkedIn connection invitations on linkedin.com?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/get_sent_invitations, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/get_sent_invitations

### Is there a linkedin.com API to get sent LinkedIn connection invitations?

You do not need one. "Get sent LinkedIn connection invitations" drives the real linkedin.com pages in a browser, so it works whether or not linkedin.com offers an API for this.

### What information do I need to provide?

Optional: limit.

### What does it return?

It returns total, invitations.

### Do I need to be logged in to linkedin.com?

Yes. It acts as you on linkedin.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the linkedin.com cookies saved by the Reduck extension.

### Does it change anything on linkedin.com, or only read data?

It only reads. It looks things up on linkedin.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/get_sent_invitations, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/get_sent_invitations

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/linkedin.com/get_sent_invitations
