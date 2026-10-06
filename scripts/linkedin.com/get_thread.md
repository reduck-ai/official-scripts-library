# Get LinkedIn message thread

Automatically get LinkedIn message thread on linkedin.com. You get the latest messages from one private conversation, in order, ready to log or reply to.

- Site: linkedin.com
- Address: `reduck/linkedin.com/get_thread`
- Updated: 2026-10-05 (v5)
- Author: Reduck AI (reduck)

## About

A candidate's salary answer, a warm intro from a former colleague: on LinkedIn that stuff sits in DMs, not email. Give it the URL of one conversation and you get the messages LinkedIn loads with it, oldest first, plus sender names and the other people in the chat when it is one of your recent conversations. On a recruiter's Monday, list_inbox with unreadOnly and a sinceIso of Saturday turns up nine conversations from the weekend, get_thread reads each one, and an agent copies the salary figure into the ATS and drafts the reply for send_message. That routine has two catches. LinkedIn treats opening a conversation as reading it, so those nine lose their unread badge, and mark_conversation_unread puts the badge back on any you still owe an answer. You also get only the first batch LinkedIn loads, so a two-year back-and-forth ends wherever that batch ends. If you meant the comment thread under a post, that is get_post_comments.

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/linkedin.com/get_thread`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/linkedin.com/get_thread
```

## Input

- `threadUrl` (string, required): A LinkedIn /messaging/thread/<id>/ URL, as returned by linkedin.com/list_inbox.

## FAQ

### What does "Get LinkedIn message thread" do?

Read a classic LinkedIn messaging conversation (NOT Sales Navigator) by its thread URL from list_inbox. Returns the participants and messages (from, fromSelf, text, time, subject) in chronological order. Returns the most recent page only.

### How do I automatically get LinkedIn message thread on linkedin.com?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/get_thread, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/get_thread

### Is there a linkedin.com API to get LinkedIn message thread?

You do not need one. "Get LinkedIn message thread" drives the real linkedin.com pages in a browser, so it works whether or not linkedin.com offers an API for this.

### What information do I need to provide?

Required: threadUrl.

### Do I need to be logged in to linkedin.com?

Yes. It acts as you on linkedin.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the linkedin.com cookies saved by the Reduck extension.

### Does it change anything on linkedin.com, or only read data?

It only reads. It looks things up on linkedin.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/get_thread, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/get_thread

### Who maintains it?

It is part of Reduck's official curated catalogue.

### Can I export a whole LinkedIn conversation, including old messages?

Get LinkedIn message thread stops at the most recent page LinkedIn loads when a conversation opens and does not page back for older messages. For the full history, LinkedIn's own archive under Settings & Privacy, Data privacy, Download your data has a Messages category; request only that one and the download link arrives by email within minutes, while a full archive can take up to 24 hours.

### Will the other person see that I read their message?

Opening a conversation with Get LinkedIn message thread counts as reading it, so the sender will likely see your profile photo appear next to their message, which is LinkedIn's read receipt. The switch is under Settings & Privacy, Data privacy, Delivery and typing indicators, and when it is off nobody in the conversation, you included, can see whether messages were read.

### Why are sender names missing on some LinkedIn threads?

When a conversation is not among the roughly 20 most recent ones LinkedIn syncs on page load, the messages still come back with text and timestamps, but participants is empty, from and fromSelf are null, and participantsResolved is false. The sibling linkedin.com/get_chat_attendees takes the same thread URL and still lists who is in the conversation, falling back to whoever has spoken when the full roster is not loaded. What neither gives you for an older thread is which side wrote each message.

### Can it read Sales Navigator messages or download attachments?

Get LinkedIn message thread reads only the classic inbox, and only the text and subject of each message. Sales Navigator conversations need linkedin.com/sales_navigator_get_thread (and a Sales Navigator seat), while the file behind an image or document message comes from linkedin.com/get_message_attachment, which takes the same thread URL.

Source: https://reduck.ai/explore/scripts/reduck/linkedin.com/get_thread
