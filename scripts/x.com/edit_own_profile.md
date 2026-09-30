# Edit your X (Twitter) profile: name, bio, location, website

Update the signed-in X (Twitter) account's own display name (50 characters at most), bio (160), location (30) and website link (100). Omit a field to leave it unchanged; an empty string clears the bio, the location or the website. Returns the profile's name, bio, location and url after the edit.

- Site: x.com
- Address: `reduck/x.com/edit_own_profile`
- Updated: 2026-09-29 (v1)
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

### What does "Edit your X (Twitter) profile: name, bio, location, website" do?

Update the signed-in X (Twitter) account's own display name (50 characters at most), bio (160), location (30) and website link (100). Omit a field to leave it unchanged; an empty string clears the bio, the location or the website. Returns the profile's name, bio, location and url after the edit.

### What information do I need to provide?

Optional: bio, url, name, location.

### What does it return?

It returns bio, url, name, location.

### Do I need to be logged in to x.com?

Yes. It acts as you on x.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the x.com cookies saved by the Reduck extension.

### Does it change anything on x.com, or only read data?

It makes changes on x.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/x.com/edit_own_profile, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/x.com/edit_own_profile

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/x.com/edit_own_profile
