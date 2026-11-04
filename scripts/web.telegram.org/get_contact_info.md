# Telegram — Get a person's contact info

Automatically get a person's contact info on web.telegram.org. Read a Telegram user's profile: display name, username, bio, presence line and phone number, given their user id (the userId web.telegram.org/get_group_members returns, or a person's peerId from web.telegram.org/get_inbox). A field Telegram does not show comes back null; the phone in particular shows only for contacts who share it, so null means not visible to this account. It never marks anything read: when the conversation with that person has unread messages, it refuses and asks you to read them first. Group and channel ids, and your own id, are refused with a message that says what to use instead.

- Site: web.telegram.org
- Address: `reduck/web.telegram.org/get_contact_info`
- Updated: 2026-11-03 (v4)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/web.telegram.org/get_contact_info`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/web.telegram.org/get_contact_info
```

## Input

- `peerId` (string, required): The person's Telegram user id — a positive integer, e.g. "93372553". get_group_members returns exactly this as each member's userId. Group and channel ids are negative and are refused, since they have no contact info. Your own id is refused too — Telegram routes it to Saved Messages; use get_own_profile for yourself.

## Output

- `name` (string | null, required): The person's display name as the profile renders it.
- `peerId` (string, required): The user id that was actually opened, read back from the address bar.
- `verified_on_page` (boolean, required): True when the fields were read from a rendered profile panel, rather than an empty panel being reported as a profile with no details.
- `bio` (string | null, optional): The bio / about text, or null when empty. For a bot this is its description.
- `phone` (string | null, optional): The phone number as Telegram displays it, or null when no phone row is shown. Null does NOT mean the person has no phone — Telegram only shows it for contacts who share it, so treat null as "not visible to this account". Unverified against a populated row: the account used for development has no contacts, so only the absent case was observed.
- `username` (string | null, optional): Their @username without the leading @, or null when they have none. Located by the panel's mention icon, not by the translated "Username" label beside it.
- `statusLabel` (string | null, optional): The line under the name — presence for a person (online, last seen recently), or the monthly-user count for a bot. Telegram's own wording, so translated: treat as display text, not a state to branch on.

## FAQ

### What does "Telegram — Get a person's contact info" do?

Read a Telegram user's profile: display name, username, bio, presence line and phone number, given their user id (the userId web.telegram.org/get_group_members returns, or a person's peerId from web.telegram.org/get_inbox). A field Telegram does not show comes back null; the phone in particular shows only for contacts who share it, so null means not visible to this account. It never marks anything read: when the conversation with that person has unread messages, it refuses and asks you to read them first. Group and channel ids, and your own id, are refused with a message that says what to use instead.

### How do I automatically get a person's contact info on web.telegram.org?

Ask an AI agent connected to Reduck to run reduck/web.telegram.org/get_contact_info, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/web.telegram.org/get_contact_info

### Is there a web.telegram.org API to get a person's contact info?

You do not need one. "Telegram — Get a person's contact info" drives the real web.telegram.org pages in a browser, so it works whether or not web.telegram.org offers an API for this.

### What information do I need to provide?

Required: peerId.

### What does it return?

It returns bio, name, phone, peerId, username, statusLabel, verified_on_page.

### Do I need to be logged in to web.telegram.org?

Yes. It acts as you on web.telegram.org: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the web.telegram.org cookies saved by the Reduck extension.

### Does it change anything on web.telegram.org, or only read data?

It only reads. It looks things up on web.telegram.org and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/web.telegram.org/get_contact_info, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/web.telegram.org/get_contact_info

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/web.telegram.org/get_contact_info
