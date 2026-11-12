# List a Telegram group's members

Automatically list a Telegram group's members on web.telegram.org. List the members of a Telegram group: user id, name, username, role (owner, admin or member), custom title and join date, with the total member count. Returns 200 members a page: pass nextOffset for the next page. Refuses a one-to-one conversation, and a channel whose member list only its admins can see. A group that hides its member list shows only its admins to other members. Does not mark the group as read.

- Site: web.telegram.org
- Address: `reduck/web.telegram.org/get_group_members`
- Updated: 2026-11-11 (v4)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/web.telegram.org/get_group_members`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/web.telegram.org/get_group_members
```

## Input

- `peerId` (string, required): The group: its peerId from web.telegram.org/get_inbox (a negative integer), or a public @username.
- `offset` (integer, optional): Omit for the first page. For the next one, pass the nextOffset of the previous call.

## Output

- `peerId` (string, required)
- `members` (array, required): Up to 200 members. A group whose admins hid the member list shows only its admins to other members: then the list is shorter than membersCount and nextOffset is null.
- `nextOffset` (integer | null, required): Pass it as offset for the next page. Null on the last page.
- `title` (string | null, optional)
- `membersCount` (integer | null, optional): How many members the group has in all.

## FAQ

### What does "List a Telegram group's members" do?

List the members of a Telegram group: user id, name, username, role (owner, admin or member), custom title and join date, with the total member count. Returns 200 members a page: pass nextOffset for the next page. Refuses a one-to-one conversation, and a channel whose member list only its admins can see. A group that hides its member list shows only its admins to other members. Does not mark the group as read.

### How do I automatically list a Telegram group's members on web.telegram.org?

Ask an AI agent connected to Reduck to run reduck/web.telegram.org/get_group_members, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/web.telegram.org/get_group_members

### Is there a web.telegram.org API to list a Telegram group's members?

You do not need one. "List a Telegram group's members" drives the real web.telegram.org pages in a browser, so it works whether or not web.telegram.org offers an API for this.

### What information do I need to provide?

Required: peerId. Optional: offset.

### What does it return?

It returns title, peerId, members, nextOffset, membersCount.

### Do I need to be logged in to web.telegram.org?

Yes. It acts as you on web.telegram.org: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the web.telegram.org cookies saved by the Reduck extension.

### Does it change anything on web.telegram.org, or only read data?

It only reads. It looks things up on web.telegram.org and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/web.telegram.org/get_group_members, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/web.telegram.org/get_group_members

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/web.telegram.org/get_group_members
