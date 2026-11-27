# Send a message in a Muse chat (muse.ai)

Automatically send a message in a Muse chat (muse.ai) on muse.ai. Continue a chat of the signed-in Muse account (Meta's personal agent at muse.ai): send one message in the chat you name, the main chat or a side chat, wait until Muse ends its reply (up to about 3 minutes), and return what Muse posted. Muse answers with the whole chat as its context. The output has the same fields as muse.ai/ask: `answer` joins the text of every reply message of the turn, `messages` lists the turn in order (`reply` items are Muse's text messages, `widget` items are the cards it shows, such as a browser task or shopping results), and `sources` are the pages Muse's searches gave it, deduplicated by url.

- Site: muse.ai
- Address: `reduck/muse.ai/send_message`
- Updated: 2026-11-25 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/muse.ai/send_message`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/muse.ai/send_message
```

## Input

- `chat_id` (string, required): The chat to send the message in: an id from muse.ai/list_chats or muse.ai/search_chats, or the threadId of muse.ai/ask.
- `message` (string, required): The message to send. Line breaks are kept. It must hold at least one character that is not a space.

## Output

- `url` (string, required): Where the chat opens on muse.ai: https://muse.ai/ for the main chat, https://muse.ai/thread/<chatId> for a side chat.
- `answer` (string, required): The markdown of every reply message of the turn, in order, separated by a blank line. Links keep their real address.
- `chatId` (string, required): The id of the chat the message was sent in.
- `pending` (boolean | null, required): True when Muse is still working on the message as the run returns: the answer is then its first reply, and Muse posts its result later in the chat. False when the work is done or used no tool. Null when the browser hides Muse's activity panel, so the run cannot tell.
- `sources` (array, required): Every source of the turn's messages, deduplicated by url, in order of first appearance.
- `messages` (array, required): What Muse posted in reply to the message when the run returned, in order.

## FAQ

### What does "Send a message in a Muse chat (muse.ai)" do?

Continue a chat of the signed-in Muse account (Meta's personal agent at muse.ai): send one message in the chat you name, the main chat or a side chat, wait until Muse ends its reply (up to about 3 minutes), and return what Muse posted. Muse answers with the whole chat as its context. The output has the same fields as muse.ai/ask: `answer` joins the text of every reply message of the turn, `messages` lists the turn in order (`reply` items are Muse's text messages, `widget` items are the cards it shows, such as a browser task or shopping results), and `sources` are the pages Muse's searches gave it, deduplicated by url.

### How do I automatically send a message in a Muse chat (muse.ai) on muse.ai?

Ask an AI agent connected to Reduck to run reduck/muse.ai/send_message, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/muse.ai/send_message

### Is there a muse.ai API to send a message in a Muse chat (muse.ai)?

You do not need one. "Send a message in a Muse chat (muse.ai)" drives the real muse.ai pages in a browser, so it works whether or not muse.ai offers an API for this.

### What information do I need to provide?

Required: chat_id, message.

### What does it return?

It returns url, answer, chatId, pending, sources, messages.

### Do I need to be logged in to muse.ai?

Yes. It acts as you on muse.ai: in your browser it reuses your session, and on a cloud browser it loads your Auth session cookies for muse.ai.

### Does it change anything on muse.ai, or only read data?

It makes changes on muse.ai, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/muse.ai/send_message, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/muse.ai/send_message

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/muse.ai/send_message
