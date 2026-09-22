# React to a Telegram message

Automatically react to a Telegram message on web.telegram.org. Add your reaction to a Telegram message, or take it back with remove:true, given the conversation's peer id, the message id and the emoji. Scope: the emoji must already be one of the reactions on that message — Telegram's reaction picker renders each choice as an animated canvas with no machine-readable identity, so a brand-new reaction type cannot be selected reliably, and this reports which emojis are available rather than clicking a guess. Resolves the emoji through Telegram's own reactions table instead of any translated label, confirms the change by the reaction pill's chosen state, and refuses Saved Messages, where the same-looking picker applies tags rather than reactions.

- Site: web.telegram.org
- Address: `reduck/web.telegram.org/react_to_message`
- Updated: 2026-09-16 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/web.telegram.org/react_to_message`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/web.telegram.org/react_to_message
```

## Input

- `emoji` (string, required): The reaction emoji as a character, e.g. "❤", "🔥", "😭". It must already appear as a reaction on the target message; the script tells you which emojis qualify when it does not. Resolved through Telegram's own reactions table, so it is matched by identity rather than by any translated emoji name.
- `peerId` (string, required): The conversation's peer id, as returned by get_inbox (negative ids are channels and groups). Saved Messages is refused — see the description.
- `messageId` (string, required): The message to react to, as returned by get_conversation. Must be in the recently loaded window of that conversation.
- `remove` (boolean, optional): Leave false (the default) to add your reaction. Set true to take your own reaction back. Both are the same toggle in Telegram, which is why this is a flag rather than a second script.

## Output

- `emoji` (string, required): The emoji that was reacted with.
- `peerId` (string, required): The peer id that was actually opened, read back from the address bar.
- `changed` (boolean, required): True when this run actually flipped your reaction. False means it was already in the requested state and nothing was clicked.
- `messageId` (string, required): The message that was acted on.
- `reactedNow` (boolean, required): Whether your reaction is on the message after this ran, read back from the pill's chosen state rather than assumed from the click.
- `account_used` (string | null, required): The account that reacted, read from the app's own account menu rather than assumed from the request. Null if the menu did not expose a name.
- `already_in_state` (boolean, required): True when your reaction was already present (or already absent) before this ran, so the request was a no-op.
- `verified_on_page` (boolean, required): True when the resulting state was confirmed by the pill's chosen state on the page, rather than assumed from the click.
- `chatTitle` (string | null, optional): The conversation title from the header — echo this to a human, since a peer id is not recognisable.
- `countAfter` (integer | null, optional): The reaction's total count afterwards, read from the pill this script clicked once it settled. Null only when that pill is gone entirely, which happens when you removed the last reaction of that type. On a busy channel other people react at the same time, so treat the delta as indicative and reactedNow as authoritative.
- `emojiTitle` (string | null, optional): Telegram's own name for that emoji, taken from its reactions table (e.g. "Red Heart" for ❤). This is how the script located the right reaction pill without depending on a hardcoded label.
- `countBefore` (integer | null, optional): The reaction's total count before the click, as Telegram rendered it.
- `replacedEmoji` (string | null, optional): The emoji whose reaction this displaced, or null if none. Telegram allows only one reaction per message on a standard account, so adding one SILENTLY removes the one you had before — this field makes that visible instead of leaving the caller to discover it. Always null when removing.
- `availableOnMessage` (array, optional): The emojis that currently have a reaction group on this message, which are the ones this script can act on.

## FAQ

### What does "React to a Telegram message" do?

Add your reaction to a Telegram message, or take it back with remove:true, given the conversation's peer id, the message id and the emoji. Scope: the emoji must already be one of the reactions on that message — Telegram's reaction picker renders each choice as an animated canvas with no machine-readable identity, so a brand-new reaction type cannot be selected reliably, and this reports which emojis are available rather than clicking a guess. Resolves the emoji through Telegram's own reactions table instead of any translated label, confirms the change by the reaction pill's chosen state, and refuses Saved Messages, where the same-looking picker applies tags rather than reactions.

### How do I automatically react to a Telegram message on web.telegram.org?

Ask an AI agent connected to Reduck to run reduck/web.telegram.org/react_to_message, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/web.telegram.org/react_to_message

### Is there a web.telegram.org API to react to a Telegram message?

You do not need one. "React to a Telegram message" drives the real web.telegram.org pages in a browser, so it works whether or not web.telegram.org offers an API for this.

### What information do I need to provide?

Required: peerId, messageId, emoji. Optional: remove.

### What does it return?

It returns emoji, peerId, changed, chatTitle, messageId, countAfter, emojiTitle, reactedNow, countBefore, account_used, replacedEmoji, already_in_state, verified_on_page, availableOnMessage.

### Do I need to be logged in to web.telegram.org?

Yes. It acts as you on web.telegram.org: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the web.telegram.org cookies saved by the Reduck extension.

### Does it change anything on web.telegram.org, or only read data?

It makes changes on web.telegram.org, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/web.telegram.org/react_to_message, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/web.telegram.org/react_to_message

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/web.telegram.org/react_to_message
