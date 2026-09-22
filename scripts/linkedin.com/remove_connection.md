# Remove LinkedIn connection

Automatically remove LinkedIn connection on linkedin.com. Permanently remove an existing 1st-degree LinkedIn connection by profile URL, via the profile's overflow menu -> Remove connection -> confirm. This ends a real connection, not a pending invite (use `withdraw` to cancel one of those instead) — the other person is not notified, but reconnecting afterward means sending a brand-new invitation and having them accept it again. Safe to repeat: it returns not_connected if the profile isn't currently a 1st-degree connection, instead of guessing.

- Site: linkedin.com
- Address: `reduck/linkedin.com/remove_connection`
- Updated: 2026-09-03 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/linkedin.com/remove_connection`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/linkedin.com/remove_connection
```

## Input

- `profileUrl` (string, required): LinkedIn profile URL, e.g. https://www.linkedin.com/in/jolz/

## Output

- `status` (string, required): removed = the connection was just ended; not_connected = this profile wasn't a 1st-degree connection to begin with.
- `publicId` (string, required): vanity id parsed from the URL (decoded)
- `profileUrl` (string, required)
- `name` (string | null, optional)

## FAQ

### What does "Remove LinkedIn connection" do?

Permanently remove an existing 1st-degree LinkedIn connection by profile URL, via the profile's overflow menu -> Remove connection -> confirm. This ends a real connection, not a pending invite (use `withdraw` to cancel one of those instead) — the other person is not notified, but reconnecting afterward means sending a brand-new invitation and having them accept it again. Safe to repeat: it returns not_connected if the profile isn't currently a 1st-degree connection, instead of guessing.

### How do I automatically remove LinkedIn connection on linkedin.com?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/remove_connection, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/remove_connection

### Is there a linkedin.com API to remove LinkedIn connection?

You do not need one. "Remove LinkedIn connection" drives the real linkedin.com pages in a browser, so it works whether or not linkedin.com offers an API for this.

### What information do I need to provide?

Required: profileUrl.

### What does it return?

It returns name, status, publicId, profileUrl.

### Do I need to be logged in to linkedin.com?

Yes. It acts as you on linkedin.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the linkedin.com cookies saved by the Reduck extension.

### Does it change anything on linkedin.com, or only read data?

It makes changes on linkedin.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/remove_connection, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/remove_connection

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/linkedin.com/remove_connection
