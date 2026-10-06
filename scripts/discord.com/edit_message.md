# Edit Discord message

Automatically edit Discord message on discord.com. Correct one of your own server messages and keep a copy of what it said before.

- Site: discord.com
- Address: `reduck/discord.com/edit_message`
- Updated: 2026-10-05 (v13)
- Author: Reduck AI (reduck)

## About

In the Discord app you hover over the message and click the pencil, or press the up arrow to edit your last one. You would only hand this to an agent already doing Discord work for you, when the fix is part of that job. Say the meetup announcement in #announcements went out with 8pm instead of 9pm. Copy its link (right-click, Copy Message Link) and send the full corrected text. You get back what Discord saved, plus previousContent with the old wording as the edit box showed it. The catch is that an edit pings nobody. Anyone who saw 8pm in a notification still has 8pm in their head, so a short reply under the announcement (discord.com/reply_to_message) does more than the (edited) tag. Your text replaces the whole message and is capped at 2000 characters, even though Nitro accounts can post 4000. Only your own messages in server channels and threads can be changed, not DMs.

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/discord.com/edit_message`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/discord.com/edit_message
```

## Input

- `content` (string, required): The full replacement text. This replaces the message entirely, it does not append.
- `messageUrl` (string, required): Full url of your own message, e.g. https://discord.com/channels/<guildId>/<channelId>/<messageId>. discord.com/read_messages or discord.com/search_messages return the ids to build one.

## Output

- `edited` (boolean, required)
- `content` (string, required)
- `channelId` (string, required)
- `messageId` (string, required)
- `previousContent` (string | null, required)
- `editedTimestamp` (string | null, optional)

## Example output

Shape only: placeholder values generated from the output schema, not a real run.

```json
{
  "edited": true,
  "content": "…",
  "channelId": "abc123",
  "messageId": "abc123",
  "editedTimestamp": "…",
  "previousContent": "…"
}
```

## FAQ

### What does "Edit Discord message" do?

Edit the text of one of your own Discord messages, addressed by its url. Discord marks an edited message with an "(edited)" tag visible to everyone. Returns the message's id, channel id, the new content as Discord stored it, and the edit timestamp. Only your own messages can be edited — Discord's UI offers no edit control on anyone else's.

### How do I automatically edit Discord message on discord.com?

Ask an AI agent connected to Reduck to run reduck/discord.com/edit_message, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/discord.com/edit_message

### Is there a discord.com API to edit Discord message?

You do not need one. "Edit Discord message" drives the real discord.com pages in a browser, so it works whether or not discord.com offers an API for this.

### What information do I need to provide?

Required: messageUrl, content.

### What does it return?

It returns edited, content, channelId, messageId, editedTimestamp, previousContent.

### Do I need to be logged in to discord.com?

Yes. It acts as you on discord.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the discord.com cookies saved by the Reduck extension.

### Does it change anything on discord.com, or only read data?

It makes changes on discord.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/discord.com/edit_message, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/discord.com/edit_message

### Who maintains it?

It is part of Reduck's official curated catalogue.

### Can people see that I edited a Discord message, and what it said before?

Everyone who can see the message gets an (edited) label next to it, but Discord shows readers no edit history. In a server, a logging bot set up to record edits (Carl-bot, for one, posts the before and after text) may have kept the old version. The edit_message script hands you the old wording as previousContent, and if you need it exact, with mentions as <@id>, read the message first with discord.com/read_messages.

### Can I edit an old Discord message?

Yes, if you wrote it: Discord does not appear to put a time limit on editing your own messages. Reduck's edit_message script opens the message's own link, which makes Discord jump to it in the channel. If the message still has not appeared about 20 seconds after the channel loads, the run stops with an error and the message is left as it was.

### Can a server moderator edit someone else's Discord message?

Not the text: only the author can change what a message says. A moderator with Manage Messages can hide its embeds, such as link previews, or delete it outright (discord.com/delete_message does that), but cannot rewrite a word. If Edit is missing from the message's right-click menu, the edit is refused and nothing changes.

### Can it edit a message I sent in a Discord DM?

No, Reduck's edit_message script needs a server message link (discord.com/channels/<server>/<channel>/<message>), so a DM or group DM link, which starts with discord.com/channels/@me/, is refused before the message is opened and nothing changes. Messages in server channels, threads and forum posts work.

Source: https://reduck.ai/explore/scripts/reduck/discord.com/edit_message
