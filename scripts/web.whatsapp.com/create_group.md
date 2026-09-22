# WhatsApp — Create group

Automatically create group on web.whatsapp.com. Create a WhatsApp group with a title and a list of contacts, each named exactly. Returns the created group and its members. Everyone added is notified. Optionally sends a first message into the new group, which also makes it findable by name straight away for follow-up scripts.

- Site: web.whatsapp.com
- Address: `reduck/web.whatsapp.com/create_group`
- Updated: 2026-08-26 (v16)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/web.whatsapp.com/create_group`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/create_group
```

## Input

- `name` (string, required): Group subject (title)
- `members` (array, required): Contact names to add. Each name must match the contact's display name exactly.
- `seedMessage` (string, optional): Optional: send this text into the new group immediately after creation. WhatsApp does not index a brand-new, message-less group in its own search box until it has at least one real message, so a group created without this can be briefly unfindable by name for follow-up scripts (e.g. delete_chat, leave_group, send_message). Pass a short text here to make the group immediately searchable. Off by default — omit to skip (no extra message sent).

## Output

- `group` (string, required)
- `created` (boolean, required)
- `members` (array, required)
- `seedMessageSent` (boolean, optional): Present only if seedMessage was provided; whether it was sent without WhatsApp flagging a send failure.

## FAQ

### What does "WhatsApp — Create group" do?

Create a WhatsApp group with a title and a list of contacts, each named exactly. Returns the created group and its members. Everyone added is notified. Optionally sends a first message into the new group, which also makes it findable by name straight away for follow-up scripts.

### How do I automatically create group on web.whatsapp.com?

Ask an AI agent connected to Reduck to run reduck/web.whatsapp.com/create_group, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/create_group

### Is there a web.whatsapp.com API to create group?

You do not need one. "WhatsApp — Create group" drives the real web.whatsapp.com pages in a browser, so it works whether or not web.whatsapp.com offers an API for this.

### What information do I need to provide?

Required: name, members. Optional: seedMessage.

### What does it return?

It returns group, created, members, seedMessageSent.

### Do I need to be logged in to web.whatsapp.com?

Yes. It acts as you on web.whatsapp.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the web.whatsapp.com cookies saved by the Reduck extension.

### Does it change anything on web.whatsapp.com, or only read data?

It makes changes on web.whatsapp.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/web.whatsapp.com/create_group, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/create_group

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/web.whatsapp.com/create_group
