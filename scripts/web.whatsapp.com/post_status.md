# Post text status

Automatically post text status on web.whatsapp.com. Posts a text Status update (visible to contacts for 24h) to the signed-in WhatsApp account.

- Site: web.whatsapp.com
- Address: `reduck/web.whatsapp.com/post_status`
- Updated: 2026-09-22 (v5)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/web.whatsapp.com/post_status`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/post_status
```

## Input

- `text` (string, required): The status text to post.

## Output

- `posted` (boolean, required)
- `postedAt` (string, required): The timestamp label WhatsApp shows next to My status after posting (e.g. "Today at 15:52").

## FAQ

### What does "Post text status" do?

Posts a text Status update (visible to contacts for 24h) to the signed-in WhatsApp account.

### How do I automatically post text status on web.whatsapp.com?

Ask an AI agent connected to Reduck to run reduck/web.whatsapp.com/post_status, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/post_status

### Is there a web.whatsapp.com API to post text status?

You do not need one. "Post text status" drives the real web.whatsapp.com pages in a browser, so it works whether or not web.whatsapp.com offers an API for this.

### What information do I need to provide?

Required: text.

### What does it return?

It returns posted, postedAt.

### Do I need to be logged in to web.whatsapp.com?

Yes. It acts as you on web.whatsapp.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the web.whatsapp.com cookies saved by the Reduck extension.

### Does it change anything on web.whatsapp.com, or only read data?

It makes changes on web.whatsapp.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/web.whatsapp.com/post_status, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/post_status

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/web.whatsapp.com/post_status
