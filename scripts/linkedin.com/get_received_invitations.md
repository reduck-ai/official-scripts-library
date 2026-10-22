# Get received LinkedIn connection invitations

Automatically get received LinkedIn connection invitations on linkedin.com. Lists the pending invitations the signed-in LinkedIn user has received (Manage invitations - Received), and separately the "Suggestions for you" people LinkedIn shows below them. Each invitation has the inviter's name, headline, profile URL, mutual-connection note, type (person/event/newsletter/page) and an invitation id that accept_invitation takes. Each suggestion has name, headline, profile URL and mutual note; suggestions are not invitations and cannot be accepted. complete says whether the whole list was read; when limit stops it early, suggestions is null, because LinkedIn shows them only after the last invitation. Returns an empty invitations list when there are none.

- Site: linkedin.com
- Address: `reduck/linkedin.com/get_received_invitations`
- Updated: 2026-10-21 (v9)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/linkedin.com/get_received_invitations`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/linkedin.com/get_received_invitations
```

## Input

- `limit` (number, optional): Max invitations to return (default 100). LinkedIn loads about 10 at a time, so a lower limit means fewer loads when you only need the newest ones.

## Output

- `total` (number, required): Number of received pending invitations returned (suggestions not counted). 0 when there are none.
- `complete` (boolean, required): True when the invitation list was read to its end; false when limit stopped it first.
- `invitations` (array, required): Real pending invitations (each has Ignore + Accept).
- `suggestions` (array | null, required): 'Suggestions for you' / People you may know cards LinkedIn shows below the end of the invitation list (a Connect button, not an invitation). null when complete is false: LinkedIn shows them only once the list has ended.

## FAQ

### What does "Get received LinkedIn connection invitations" do?

Lists the pending invitations the signed-in LinkedIn user has received (Manage invitations - Received), and separately the "Suggestions for you" people LinkedIn shows below them. Each invitation has the inviter's name, headline, profile URL, mutual-connection note, type (person/event/newsletter/page) and an invitation id that accept_invitation takes. Each suggestion has name, headline, profile URL and mutual note; suggestions are not invitations and cannot be accepted. complete says whether the whole list was read; when limit stops it early, suggestions is null, because LinkedIn shows them only after the last invitation. Returns an empty invitations list when there are none.

### How do I automatically get received LinkedIn connection invitations on linkedin.com?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/get_received_invitations, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/get_received_invitations

### Is there a linkedin.com API to get received LinkedIn connection invitations?

You do not need one. "Get received LinkedIn connection invitations" drives the real linkedin.com pages in a browser, so it works whether or not linkedin.com offers an API for this.

### What information do I need to provide?

Optional: limit.

### What does it return?

It returns total, complete, invitations, suggestions.

### Do I need to be logged in to linkedin.com?

Yes. It acts as you on linkedin.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the linkedin.com cookies saved by the Reduck extension.

### Does it change anything on linkedin.com, or only read data?

It only reads. It looks things up on linkedin.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/get_received_invitations, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/get_received_invitations

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/linkedin.com/get_received_invitations
