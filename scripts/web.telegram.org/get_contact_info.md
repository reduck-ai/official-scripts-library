# Get a Telegram user's profile

Automatically get a Telegram user's profile on web.telegram.org. Read the Telegram profile of a person or a bot: name, username, phone (when they share it with this account), bio, birthday, the contact, bot, premium and verified flags, and presence, with the exact last-seen time when Telegram shows it. Takes a user id or a public @username; the signed-in account's own id returns its own profile. Refuses group and channel ids. Does not mark any conversation as read.

- Site: web.telegram.org
- Address: `reduck/web.telegram.org/get_contact_info`
- Updated: 2026-11-11 (v5)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/web.telegram.org/get_contact_info`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/web.telegram.org/get_contact_info
```

## Input

- `userId` (string, required): The person or bot: a user id (the userId web.telegram.org/get_group_members returns, or the peerId of a one-to-one chat from get_inbox), or a public @username.

## Output

- `name` (string | null, required)
- `userId` (string, required)
- `bio` (string | null, optional): The about text; for a bot, its description.
- `isBot` (boolean, optional)
- `phone` (string | null, optional): Digits with the country code. Null when this person does not share it with this account.
- `birthday` (string | null, optional): MM-DD, or YYYY-MM-DD when the year is shown. Null when hidden or not set.
- `presence` (string, optional): What Telegram shows: offline comes with lastSeenAt; the others are all Telegram shares when the person hides the exact time.
- `username` (string | null, optional)
- `isContact` (boolean, optional): True when this person is in the account's contacts.
- `isPremium` (boolean, optional)
- `isVerified` (boolean, optional)
- `lastSeenAt` (string | null, optional)

## FAQ

### What does "Get a Telegram user's profile" do?

Read the Telegram profile of a person or a bot: name, username, phone (when they share it with this account), bio, birthday, the contact, bot, premium and verified flags, and presence, with the exact last-seen time when Telegram shows it. Takes a user id or a public @username; the signed-in account's own id returns its own profile. Refuses group and channel ids. Does not mark any conversation as read.

### How do I automatically get a Telegram user's profile on web.telegram.org?

Ask an AI agent connected to Reduck to run reduck/web.telegram.org/get_contact_info, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/web.telegram.org/get_contact_info

### Is there a web.telegram.org API to get a Telegram user's profile?

You do not need one. "Get a Telegram user's profile" drives the real web.telegram.org pages in a browser, so it works whether or not web.telegram.org offers an API for this.

### What information do I need to provide?

Required: userId.

### What does it return?

It returns bio, name, isBot, phone, userId, birthday, presence, username, isContact, isPremium, isVerified, lastSeenAt.

### Do I need to be logged in to web.telegram.org?

Yes. It acts as you on web.telegram.org: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the web.telegram.org cookies saved by the Reduck extension.

### Does it change anything on web.telegram.org, or only read data?

It only reads. It looks things up on web.telegram.org and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/web.telegram.org/get_contact_info, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/web.telegram.org/get_contact_info

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/web.telegram.org/get_contact_info
