# Send LinkedIn connection request without note

Automatically send LinkedIn connection request without note on linkedin.com. Send a LinkedIn connection request without a note, by profile URL. Clicks the top-card Connect then "Send without a note". Only the top-card Connect is handled: profiles that show Follow as the primary action and bury Connect under the "More" overflow (influencers/public figures) return no_connect_cta. Idempotent-ish: returns status sent/pending/already_connected/no_connect_cta.

- Site: linkedin.com
- Address: `reduck/linkedin.com/connect`
- Updated: 2026-09-11 (v11)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/linkedin.com/connect`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/linkedin.com/connect
```

## Input

- `profileUrl` (string, required): LinkedIn profile URL, e.g. https://www.linkedin.com/in/ewhachen/ (the /in/<publicId> form; query/locale prefixes are tolerated).

## Output

- `status` (string, required): sent = invitation just sent without a note; pending = a request to this person was already outstanding; already_connected = 1st-degree; no_connect_cta = no Connect affordance (top card or three-dot menu) — restricted or not connectable; email_required = LinkedIn gates this member behind email verification and disabled the note-free send (can't connect without a note).
- `publicId` (string, required): vanity id parsed from the URL (decoded)
- `profileUrl` (string, required)
- `name` (string | null, optional)

## FAQ

### What does "Send LinkedIn connection request without note" do?

Send a LinkedIn connection request without a note, by profile URL. Clicks the top-card Connect then "Send without a note". Only the top-card Connect is handled: profiles that show Follow as the primary action and bury Connect under the "More" overflow (influencers/public figures) return no_connect_cta. Idempotent-ish: returns status sent/pending/already_connected/no_connect_cta.

### How do I automatically send LinkedIn connection request without note on linkedin.com?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/connect, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/connect

### Is there a linkedin.com API to send LinkedIn connection request without note?

You do not need one. "Send LinkedIn connection request without note" drives the real linkedin.com pages in a browser, so it works whether or not linkedin.com offers an API for this.

### What information do I need to provide?

Required: profileUrl.

### What does it return?

It returns name, status, publicId, profileUrl.

### Do I need to be logged in to linkedin.com?

Yes. It acts as you on linkedin.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the linkedin.com cookies saved by the Reduck extension.

### Does it change anything on linkedin.com, or only read data?

It makes changes on linkedin.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/connect, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/connect

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/linkedin.com/connect
