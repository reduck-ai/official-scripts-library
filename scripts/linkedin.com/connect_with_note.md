# Send LinkedIn connection request

Automatically send LinkedIn connection request on linkedin.com. Send a LinkedIn connection request with a personal note to a profile URL. Fails fast if the monthly note quota is exhausted or the profile isn't connectable (already 1st-degree, pending, or no Connect CTA); the note caps at 200 chars on free-tier. Returns status (sent/already_connected/pending/no_quota/no_connect_cta/failed), profileUrl, name, reason.

- Site: linkedin.com
- Address: `reduck/linkedin.com/connect_with_note`
- Updated: 2026-09-15 (v9)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/linkedin.com/connect_with_note`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/linkedin.com/connect_with_note
```

## Input

- `message` (string, required): Personal note. LinkedIn free-tier caps at 200 chars.
- `profileUrl` (string, required): Canonical LinkedIn profile URL (https://www.linkedin.com/in/<slug>/).

## Output

- `status` (any, required)
- `profileUrl` (string, required)
- `name` (string | null, optional): Person's display name as shown on their profile.
- `reason` (string | null, optional): Failure detail when status != sent.

## FAQ

### What does "Send LinkedIn connection request" do?

Send a LinkedIn connection request with a personal note to a profile URL. Fails fast if the monthly note quota is exhausted or the profile isn't connectable (already 1st-degree, pending, or no Connect CTA); the note caps at 200 chars on free-tier. Returns status (sent/already_connected/pending/no_quota/no_connect_cta/failed), profileUrl, name, reason.

### How do I automatically send LinkedIn connection request on linkedin.com?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/connect_with_note, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/connect_with_note

### Is there a linkedin.com API to send LinkedIn connection request?

You do not need one. "Send LinkedIn connection request" drives the real linkedin.com pages in a browser, so it works whether or not linkedin.com offers an API for this.

### What information do I need to provide?

Required: profileUrl, message.

### What does it return?

It returns name, reason, status, profileUrl.

### Do I need to be logged in to linkedin.com?

Yes. It acts as you on linkedin.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the linkedin.com cookies saved by the Reduck extension.

### Does it change anything on linkedin.com, or only read data?

It makes changes on linkedin.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/connect_with_note, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/connect_with_note

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/linkedin.com/connect_with_note
