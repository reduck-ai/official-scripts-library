# WhatsApp — Leave group

Automatically leave group on web.whatsapp.com. Leave (exit) a WhatsApp group by exact name, then confirm you are really out. With alsoDelete:true the conversation is also removed from your chat list; left off, the chat stays with its history. Only admins are notified when you leave. If you are already no longer a member of that group, it reports that instead of touching the conversation. Leaving removes you from the group and cannot be undone from here, so the group name is worth confirming with the user rather than guessed.

- Site: web.whatsapp.com
- Address: `reduck/web.whatsapp.com/leave_group`
- Updated: 2026-08-20 (v6)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/web.whatsapp.com/leave_group`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/leave_group
```

## Input

- `name` (string, required): Exact group name
- `alsoDelete` (boolean, optional): Also delete the chat from your list (default false = keep the chat with its history)

## Output

- `left` (boolean, required): You are no longer a member of the group
- `group` (string, required): The group name, as read from the chat that was opened
- `chatDeleted` (boolean, optional): The chat was also removed from your list (only when alsoDelete was requested)

## FAQ

### What does "WhatsApp — Leave group" do?

Leave (exit) a WhatsApp group by exact name, then confirm you are really out. With alsoDelete:true the conversation is also removed from your chat list; left off, the chat stays with its history. Only admins are notified when you leave. If you are already no longer a member of that group, it reports that instead of touching the conversation. Leaving removes you from the group and cannot be undone from here, so the group name is worth confirming with the user rather than guessed.

### How do I automatically leave group on web.whatsapp.com?

Ask an AI agent connected to Reduck to run reduck/web.whatsapp.com/leave_group, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/leave_group

### Is there a web.whatsapp.com API to leave group?

You do not need one. "WhatsApp — Leave group" drives the real web.whatsapp.com pages in a browser, so it works whether or not web.whatsapp.com offers an API for this.

### What information do I need to provide?

Required: name. Optional: alsoDelete.

### What does it return?

It returns left, group, chatDeleted.

### Do I need to be logged in to web.whatsapp.com?

Yes. It acts as you on web.whatsapp.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the web.whatsapp.com cookies saved by the Reduck extension.

### Does it change anything on web.whatsapp.com, or only read data?

It makes changes on web.whatsapp.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/web.whatsapp.com/leave_group, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/leave_group

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/web.whatsapp.com/leave_group
