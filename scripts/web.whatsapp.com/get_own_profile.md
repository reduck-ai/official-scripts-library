# WhatsApp — Get own profile

Automatically get own profile on web.whatsapp.com. Read the logged-in WhatsApp account's own profile: display name, About/status text, phone number and profile picture. If the browser isn't linked to WhatsApp, it says so straight away instead of waiting for a UI that will never load.

- Site: web.whatsapp.com
- Address: `reduck/web.whatsapp.com/get_own_profile`
- Updated: 2026-11-16 (v11)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/web.whatsapp.com/get_own_profile`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/get_own_profile
```

## Input

It takes no input.

## Output

- `loggedIn` (boolean, required): Always true on a result: an unlinked browser throws SignedOutError.
- `name` (string | null, optional): The profile's display name.
- `about` (string | null, optional): The About text, or null when none is set.
- `account` (string | null, optional): The phone number the account signs in with, digits only with country code.
- `evidence` (string | null, optional): Always null: an unlinked browser throws SignedOutError.
- `navLayout` (string | null, optional)
- `hasPicture` (boolean, optional)
- `isBusiness` (boolean, optional)
- `pictureUrl` (string | null, optional)
- `description` (string | null, optional)
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

It returns name, about, account, evidence, loggedIn, navLayout, hasPicture, isBusiness, pictureUrl, description, businessCategory.

### Do I need to be logged in to web.whatsapp.com?

Yes. It acts as you on web.whatsapp.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the web.whatsapp.com cookies saved by the Reduck extension.

### Does it change anything on web.whatsapp.com, or only read data?

It only reads. It looks things up on web.whatsapp.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/web.whatsapp.com/get_own_profile, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/get_own_profile

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/web.whatsapp.com/get_own_profile
