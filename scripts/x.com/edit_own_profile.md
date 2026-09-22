# Edit X Profile

Automatically edit X Profile on x.com. Updates this account's own display name, bio, location, and/or website link.

- Site: x.com
- Address: `reduck/x.com/edit_own_profile`
- Updated: 2026-09-03 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/x.com/edit_own_profile`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/x.com/edit_own_profile
```

## Input

- `bio` (string, optional): Bio text. X caps this at 160 characters. Pass an empty string to clear it. Omit to leave unchanged.
- `url` (string, optional): Website link shown on the profile. X caps this at 100 characters. Pass an empty string to clear it. Omit to leave unchanged.
- `name` (string, optional): Display name. X caps this at 50 characters. Omit to leave unchanged.
- `location` (string, optional): Free-text location (not geocoded). X caps this at 30 characters. Pass an empty string to clear it. Omit to leave unchanged.

## Output

- `bio` (string, required)
- `name` (string, required)
- `location` (string, required)
- `url` (string | null, optional)

## FAQ

### What does "Edit X Profile" do?

Updates this account's own display name, bio, location, and/or website link.

### How do I automatically edit X Profile on x.com?

Ask an AI agent connected to Reduck to run reduck/x.com/edit_own_profile, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/x.com/edit_own_profile

### Is there a x.com API to edit X Profile?

You do not need one. "Edit X Profile" drives the real x.com pages in a browser, so it works whether or not x.com offers an API for this.

### What information do I need to provide?

Optional: bio, url, name, location.

### What does it return?

It returns bio, url, name, location.

### Do I need to be logged in to x.com?

Yes. It acts as you on x.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the x.com cookies saved by the Reduck extension.

### Does it change anything on x.com, or only read data?

It makes changes on x.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/x.com/edit_own_profile, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/x.com/edit_own_profile

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/x.com/edit_own_profile
