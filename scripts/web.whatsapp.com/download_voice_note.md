# Download a WhatsApp voice note

Automatically download a WhatsApp voice note on web.whatsapp.com. Download one WhatsApp voice note, or audio message, to a file on the computer running the browser, and return where it was saved. Give the message by its id from get_conversation, where a voice note has the type ptt and an audio file the type audio. Returns the file's path and name, its audio format, size and duration, the chat it belongs to and when it was sent. The file is checked byte for byte against WhatsApp's own fingerprint of it before it is saved. The note is not played and the chat is not opened, so the sender does not see it as played and nothing is marked as read. Any other kind of message is refused with its kind named: images and documents go through download_media. If the browser is not linked to WhatsApp, or WhatsApp Web is open in another tab of the same browser, the run stops and says so.

- Site: web.whatsapp.com
- Address: `reduck/web.whatsapp.com/download_voice_note`
- Updated: 2026-10-22 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/web.whatsapp.com/download_voice_note`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/download_voice_note
```

## Input

- `messageId` (string, required): The voice note's message id, as get_conversation returns it in `id` (also get_inbox's lastMessage.id and search_messages' ids), e.g. false_<chat>_<key>. The message must be a voice note (type ptt) or an audio message (type audio); any other type is refused with its kind named.

## Output

- `size` (integer, required): Size of the saved file in bytes.
- `type` (any, required): ptt for a voice note recorded in WhatsApp, audio for an audio file sent as a message.
- `chatId` (string, required): The chat the note belongs to, as get_inbox returns it in `chatId`.
- `filename` (string, required): Name of the saved file. It can carry a numbered suffix when a file of that name was already there.
- `mimeType` (string, required): Audio format as WhatsApp gives it, e.g. audio/ogg; codecs=opus.
- `messageId` (string, required)
- `at` (string | null, optional): When it was sent, ISO datetime.
- `url` (string | null, optional): A link to the file, when it is not saved on the computer running the browser.
- `path` (string | null, optional): Where the file was saved on the computer running the browser.
- `fromMe` (boolean, optional)
- `durationSeconds` (integer | null, optional): Length of the recording, as WhatsApp states it.

## FAQ

### What does "Download a WhatsApp voice note" do?

Download one WhatsApp voice note, or audio message, to a file on the computer running the browser, and return where it was saved. Give the message by its id from get_conversation, where a voice note has the type ptt and an audio file the type audio. Returns the file's path and name, its audio format, size and duration, the chat it belongs to and when it was sent. The file is checked byte for byte against WhatsApp's own fingerprint of it before it is saved. The note is not played and the chat is not opened, so the sender does not see it as played and nothing is marked as read. Any other kind of message is refused with its kind named: images and documents go through download_media. If the browser is not linked to WhatsApp, or WhatsApp Web is open in another tab of the same browser, the run stops and says so.

### How do I automatically download a WhatsApp voice note on web.whatsapp.com?

Ask an AI agent connected to Reduck to run reduck/web.whatsapp.com/download_voice_note, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/download_voice_note

### Is there a web.whatsapp.com API to download a WhatsApp voice note?

You do not need one. "Download a WhatsApp voice note" drives the real web.whatsapp.com pages in a browser, so it works whether or not web.whatsapp.com offers an API for this.

### What information do I need to provide?

Required: messageId.

### What does it return?

It returns at, url, path, size, type, chatId, fromMe, filename, mimeType, messageId, durationSeconds.

### Do I need to be logged in to web.whatsapp.com?

Yes. It acts as you on web.whatsapp.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the web.whatsapp.com cookies saved by the Reduck extension.

### Does it change anything on web.whatsapp.com, or only read data?

It only reads. It looks things up on web.whatsapp.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/web.whatsapp.com/download_voice_note, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/download_voice_note

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/web.whatsapp.com/download_voice_note
