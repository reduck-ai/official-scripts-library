# Mute an Instagram DM thread

Automatically mute an Instagram DM thread on instagram.com. Mute or unmute notifications for an Instagram DM conversation, by the conversation partner's username. Muting supports a duration (1 hour, 8 hours, 24 hours, or until you turn it back on); unmuting applies immediately. Idempotent — reports if the thread is already in the requested state instead of re-toggling.

- Site: instagram.com
- Address: `reduck/instagram.com/mute_dm_thread`
- Updated: 2026-08-27 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/instagram.com/mute_dm_thread`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/instagram.com/mute_dm_thread
```

## Input

- `username` (string, required): Handle of the conversation partner, without @.
- `mute` (boolean, optional): true to mute the thread's notifications, false to unmute.
- `duration` (string, optional): How long to mute for when mute=true. Ignored when unmuting.

## Output

- `muted` (boolean, required)
- `status` (string, required)
- `username` (string, required)
- `threadId` (string | null, optional)

## FAQ

### What does "Mute an Instagram DM thread" do?

Mute or unmute notifications for an Instagram DM conversation, by the conversation partner's username. Muting supports a duration (1 hour, 8 hours, 24 hours, or until you turn it back on); unmuting applies immediately. Idempotent — reports if the thread is already in the requested state instead of re-toggling.

### How do I automatically mute an Instagram DM thread on instagram.com?

Ask an AI agent connected to Reduck to run reduck/instagram.com/mute_dm_thread, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/instagram.com/mute_dm_thread

### Is there a instagram.com API to mute an Instagram DM thread?

You do not need one. "Mute an Instagram DM thread" drives the real instagram.com pages in a browser, so it works whether or not instagram.com offers an API for this.

### What information do I need to provide?

Required: username. Optional: mute, duration.

### What does it return?

It returns muted, status, threadId, username.

### Do I need to be logged in to instagram.com?

Yes. It acts as you on instagram.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the instagram.com cookies saved by the Reduck extension.

### Does it change anything on instagram.com, or only read data?

It makes changes on instagram.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/instagram.com/mute_dm_thread, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/instagram.com/mute_dm_thread

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/instagram.com/mute_dm_thread
