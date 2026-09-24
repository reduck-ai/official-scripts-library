# Unsend an Instagram DM

Automatically unsend an Instagram DM on instagram.com. Remove a message you sent from an Instagram DM conversation, so it disappears for everyone in the thread. Identify the message by its text, or leave the text out to take back the most recent thing you sent. Only your own messages can be taken back. If the text you give matches more than one of your messages the run refuses rather than guessing which to remove, and if it matches none it says so without touching the conversation. Removal is confirmed by re-reading the conversation from Instagram itself, not from the screen, and it cannot be undone.

- Site: instagram.com
- Address: `reduck/instagram.com/unsend_message`
- Updated: 2026-09-22 (v5)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/instagram.com/unsend_message`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/instagram.com/unsend_message
```

## Input

- `threadId` (string, required): The conversation's id, as returned by the inbox listing.
- `text` (string, optional): Text of the message to take back, matched against messages you sent. Omit to take back the most recent message you sent in the conversation.

## Output

- `unsent` (boolean, required): True when a message was actually removed.
- `threadId` (string, required)
- `account_used` (string, required): Handle of the account whose message was taken back, read from the page rather than assumed.
- `already_absent` (boolean, required): True when no message of yours matched, so nothing was touched.
- `verified_on_page` (boolean, required): True when the conversation was re-read from Instagram afterwards and the message was genuinely gone.
- `messageId` (string | null, optional): Instagram's own id for the removed message, as the conversation reports it. Note this is a different identifier from the one returned when a message is sent — the two are not interchangeable.
- `messageText` (string | null, optional): Text of the message that was removed.
- `remainingCount` (number | null, optional): How many messages the conversation holds after the removal, as Instagram reports it.

## FAQ

### What does "Unsend an Instagram DM" do?

Remove a message you sent from an Instagram DM conversation, so it disappears for everyone in the thread. Identify the message by its text, or leave the text out to take back the most recent thing you sent. Only your own messages can be taken back. If the text you give matches more than one of your messages the run refuses rather than guessing which to remove, and if it matches none it says so without touching the conversation. Removal is confirmed by re-reading the conversation from Instagram itself, not from the screen, and it cannot be undone.

### How do I automatically unsend an Instagram DM on instagram.com?

Ask an AI agent connected to Reduck to run reduck/instagram.com/unsend_message, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/instagram.com/unsend_message

### Is there a instagram.com API to unsend an Instagram DM?

You do not need one. "Unsend an Instagram DM" drives the real instagram.com pages in a browser, so it works whether or not instagram.com offers an API for this.

### What information do I need to provide?

Required: threadId. Optional: text.

### What does it return?

It returns unsent, threadId, messageId, messageText, account_used, already_absent, remainingCount, verified_on_page.

### Do I need to be logged in to instagram.com?

Yes. It acts as you on instagram.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the instagram.com cookies saved by the Reduck extension.

### Does it change anything on instagram.com, or only read data?

It makes changes on instagram.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/instagram.com/unsend_message, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/instagram.com/unsend_message

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/instagram.com/unsend_message
