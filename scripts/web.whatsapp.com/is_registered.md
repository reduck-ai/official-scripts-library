# Check if a phone number is on WhatsApp

Automatically check if a phone number is on WhatsApp on web.whatsapp.com. Check whether a phone number is registered on WhatsApp, by opening WhatsApp Web's own "message this number" deep link and seeing whether it opens a chat or shows the "not on WhatsApp" dialog. Read-only: never sends anything.

- Site: web.whatsapp.com
- Address: `reduck/web.whatsapp.com/is_registered`
- Updated: 2026-09-18 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/web.whatsapp.com/is_registered`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/is_registered
```

## Input

- `phone` (string, required): Phone number in international format, digits only, no leading + (e.g. "33766765184").

## Output

- `phone` (string, required)
- `registered` (boolean, required)
- `chatTitle` (string | null, optional): The conversation header's name/number line when registered, null otherwise.

## FAQ

### What does "Check if a phone number is on WhatsApp" do?

Check whether a phone number is registered on WhatsApp, by opening WhatsApp Web's own "message this number" deep link and seeing whether it opens a chat or shows the "not on WhatsApp" dialog. Read-only: never sends anything.

### How do I automatically check if a phone number is on WhatsApp on web.whatsapp.com?

Ask an AI agent connected to Reduck to run reduck/web.whatsapp.com/is_registered, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/is_registered

### Is there a web.whatsapp.com API to check if a phone number is on WhatsApp?

You do not need one. "Check if a phone number is on WhatsApp" drives the real web.whatsapp.com pages in a browser, so it works whether or not web.whatsapp.com offers an API for this.

### What information do I need to provide?

Required: phone.

### What does it return?

It returns phone, chatTitle, registered.

### Do I need to be logged in to web.whatsapp.com?

Yes. It acts as you on web.whatsapp.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the web.whatsapp.com cookies saved by the Reduck extension.

### Does it change anything on web.whatsapp.com, or only read data?

It only reads. It looks things up on web.whatsapp.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/web.whatsapp.com/is_registered, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/is_registered

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/web.whatsapp.com/is_registered
