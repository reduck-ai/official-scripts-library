# Send a TikTok direct message

Automatically send a TikTok direct message on tiktok.com. Send a direct message to a TikTok user by @username, as the signed-in account. The message reaches a real person the moment this runs, so show the exact recipient and text to the person asking and get their confirmation first. An existing conversation is reused, otherwise one is started from the person's profile, and the thread's own header is checked against the handle you asked for before anything is typed, so a message cannot land in the wrong conversation. If the newest message in the thread is already the same text from your account, nothing is sent again. Delivery is then confirmed by re-opening the thread fresh, because a message TikTok will not deliver still shows up in the thread at first: messages refused by TikTok's content moderation, or by the recipient's privacy settings, are reported as not sent, with TikTok's own explanation, rather than counted as delivered.

- Site: tiktok.com
- Address: `reduck/tiktok.com/send_message`
- Updated: 2026-09-14 (v6)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/tiktok.com/send_message`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/tiktok.com/send_message
```

## Input

- `text` (string, required): Message text. Sent as one message, exactly as given.
- `username` (string, required): Handle of the person to message, with or without a leading @.

## Output

- `sent` (boolean, required): True when this run delivered the message.
- `text` (string, required)
- `username` (string, required): Handle the message was addressed to, as the thread header reports it.
- `already_sent` (boolean, required): True when the newest message in the thread was already this exact text from your account, so nothing was sent again.
- `verified_in_thread` (boolean, required): True when the message was still in the thread after a fresh page load, which is the only evidence TikTok really accepted it. A message that does not survive was refused, and that is reported as an error rather than as a send.
- `userId` (string | null, optional)
- `nickname` (string | null, optional)
- `account_used` (string | null, optional): Handle the message was sent from, read from the signed-in session rather than assumed.
- `conversationId` (string | null, optional): Thread the message went to; pass it to the get-conversation script to read the thread.
- `new_conversation` (boolean, optional): True when no conversation with that account existed and one was started.

## FAQ

### What does "Send a TikTok direct message" do?

Send a direct message to a TikTok user by @username, as the signed-in account. The message reaches a real person the moment this runs, so show the exact recipient and text to the person asking and get their confirmation first. An existing conversation is reused, otherwise one is started from the person's profile, and the thread's own header is checked against the handle you asked for before anything is typed, so a message cannot land in the wrong conversation. If the newest message in the thread is already the same text from your account, nothing is sent again. Delivery is then confirmed by re-opening the thread fresh, because a message TikTok will not deliver still shows up in the thread at first: messages refused by TikTok's content moderation, or by the recipient's privacy settings, are reported as not sent, with TikTok's own explanation, rather than counted as delivered.

### How do I automatically send a TikTok direct message on tiktok.com?

Ask an AI agent connected to Reduck to run reduck/tiktok.com/send_message, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/tiktok.com/send_message

### Is there a tiktok.com API to send a TikTok direct message?

You do not need one. "Send a TikTok direct message" drives the real tiktok.com pages in a browser, so it works whether or not tiktok.com offers an API for this.

### What information do I need to provide?

Required: username, text.

### What does it return?

It returns sent, text, userId, nickname, username, account_used, already_sent, conversationId, new_conversation, verified_in_thread.

### Do I need to be logged in to tiktok.com?

Yes. It acts as you on tiktok.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the tiktok.com cookies saved by the Reduck extension.

### Does it change anything on tiktok.com, or only read data?

It makes changes on tiktok.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/tiktok.com/send_message, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/tiktok.com/send_message

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/tiktok.com/send_message
