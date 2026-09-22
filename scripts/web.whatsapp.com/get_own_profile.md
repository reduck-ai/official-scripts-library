# WhatsApp — Get own profile

Automatically get own profile on web.whatsapp.com. Read the logged-in WhatsApp account's own profile: display name, About/status text, phone number and profile picture. If the browser isn't linked to WhatsApp, it says so straight away instead of waiting for a UI that will never load.

- Site: web.whatsapp.com
- Address: `reduck/web.whatsapp.com/get_own_profile`
- Updated: 2026-09-17 (v4)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/web.whatsapp.com/get_own_profile`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/get_own_profile
```

## Input

It takes no input.

## Output

- `loggedIn` (boolean, required): Whether this browser is linked to a WhatsApp account. False is a normal result, not a failure, so this can be polled on a schedule without the check counting against its own health.
- `about` (string | null, optional)
- `phone` (string | null, optional)
- `evidence` (string | null, optional): Only set when loggedIn is false: what proved the browser unlinked, so a genuine signed-out reading can be told from a broken run.
- `navLayout` (string, optional)
- `hasPicture` (boolean, optional)
- `isBusiness` (boolean, optional)
- `pictureUrl` (string | null, optional)
- `description` (string | null, optional)
- `displayName` (string | null, optional): Null when there is no session.
- `businessCategory` (string | null, optional)

## FAQ

### What does "WhatsApp — Get own profile" do?

Read the logged-in WhatsApp account's own profile: display name, About/status text, phone number and profile picture. If the browser isn't linked to WhatsApp, it says so straight away instead of waiting for a UI that will never load.

### How do I automatically get own profile on web.whatsapp.com?

Ask an AI agent connected to Reduck to run reduck/web.whatsapp.com/get_own_profile, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/get_own_profile

### Is there a web.whatsapp.com API to get own profile?

You do not need one. "WhatsApp — Get own profile" drives the real web.whatsapp.com pages in a browser, so it works whether or not web.whatsapp.com offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns about, phone, evidence, loggedIn, navLayout, hasPicture, isBusiness, pictureUrl, description, displayName, businessCategory.

### Do I need to be logged in to web.whatsapp.com?

No. It only uses pages of web.whatsapp.com that are reachable without signing in.

### Does it change anything on web.whatsapp.com, or only read data?

It only reads. It looks things up on web.whatsapp.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/web.whatsapp.com/get_own_profile, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/get_own_profile

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/web.whatsapp.com/get_own_profile
