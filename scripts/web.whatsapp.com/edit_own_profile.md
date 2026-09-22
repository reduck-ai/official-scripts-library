# Edit own profile

Automatically edit own profile on web.whatsapp.com. Edits the signed-in account's own profile description (About) on WhatsApp Web.

- Site: web.whatsapp.com
- Address: `reduck/web.whatsapp.com/edit_own_profile`
- Updated: 2026-09-18 (v5)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/web.whatsapp.com/edit_own_profile`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/edit_own_profile
```

## Input

- `about` (string, required): New profile description / About text to save.

## Output

- `about` (string, required): The description as read back from the profile panel after saving.

## FAQ

### What does "Edit own profile" do?

Edits the signed-in account's own profile description (About) on WhatsApp Web.

### How do I automatically edit own profile on web.whatsapp.com?

Ask an AI agent connected to Reduck to run reduck/web.whatsapp.com/edit_own_profile, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/edit_own_profile

### Is there a web.whatsapp.com API to edit own profile?

You do not need one. "Edit own profile" drives the real web.whatsapp.com pages in a browser, so it works whether or not web.whatsapp.com offers an API for this.

### What information do I need to provide?

Required: about.

### What does it return?

It returns about.

### Do I need to be logged in to web.whatsapp.com?

Yes. It acts as you on web.whatsapp.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the web.whatsapp.com cookies saved by the Reduck extension.

### Does it change anything on web.whatsapp.com, or only read data?

It makes changes on web.whatsapp.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/web.whatsapp.com/edit_own_profile, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/edit_own_profile

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/web.whatsapp.com/edit_own_profile
