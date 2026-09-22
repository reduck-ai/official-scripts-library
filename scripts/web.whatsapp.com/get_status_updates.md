# Get WhatsApp Status Updates

Automatically get WhatsApp Status Updates on web.whatsapp.com. Reads the list of contacts' recent Status updates (name, timestamp, whether already viewed).

- Site: web.whatsapp.com
- Address: `reduck/web.whatsapp.com/get_status_updates`
- Updated: 2026-09-03 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/web.whatsapp.com/get_status_updates`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/get_status_updates
```

## Input

It takes no input.

## Output

- `statuses` (array, required)

## FAQ

### What does "Get WhatsApp Status Updates" do?

Reads the list of contacts' recent Status updates (name, timestamp, whether already viewed).

### How do I automatically get WhatsApp Status Updates on web.whatsapp.com?

Ask an AI agent connected to Reduck to run reduck/web.whatsapp.com/get_status_updates, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/get_status_updates

### Is there a web.whatsapp.com API to get WhatsApp Status Updates?

You do not need one. "Get WhatsApp Status Updates" drives the real web.whatsapp.com pages in a browser, so it works whether or not web.whatsapp.com offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns statuses.

### Do I need to be logged in to web.whatsapp.com?

Yes. It acts as you on web.whatsapp.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the web.whatsapp.com cookies saved by the Reduck extension.

### Does it change anything on web.whatsapp.com, or only read data?

It only reads. It looks things up on web.whatsapp.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/web.whatsapp.com/get_status_updates, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/get_status_updates

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/web.whatsapp.com/get_status_updates
