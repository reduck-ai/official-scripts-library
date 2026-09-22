# Telegram — List a group's members

Automatically list a group's members on web.telegram.org. List the members of a Telegram group, each with their user id, display name, role label and presence, read from the group's own info panel. Returns the member total Telegram reports alongside the rows actually read, so a partially loaded list is visible rather than silently short. Refuses a conversation that exposes no member list at all, which is what a broadcast channel does for anyone who is not an admin. Note that opening the conversation marks it read.

- Site: web.telegram.org
- Address: `reduck/web.telegram.org/get_group_members`
- Updated: 2026-09-03 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/web.telegram.org/get_group_members`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/web.telegram.org/get_group_members
```

## Input

- `peerId` (string, required): The group's peer id, as returned by get_inbox (groups and channels are negative, e.g. "-5521853307"). A broadcast channel you do not administer has no member list and is refused.

## Output

- `peerId` (string, required): The peer id that was actually opened, read back from the address bar.
- `members` (array, required): The member rows read from the panel, in the order the panel lists them.
- `complete` (boolean, required): True when membersRead matches the total Telegram reports, so nothing was left unloaded. False means the list is partial — large groups load lazily and this reports the shortfall rather than passing off a truncated list as the whole membership.
- `membersRead` (integer, required): How many member rows were actually read. Equal to members.length; kept as its own field so a short read is obvious next to membersCount.
- `verified_on_page` (boolean, required): True when the members were read from a rendered member list, rather than an empty panel being reported as an empty group.
- `chatTitle` (string | null, optional): The group's title — echo this to a human, since a peer id is not recognisable.
- `membersCount` (integer | null, optional): The member total Telegram reports on the group's profile, parsed from the digits in its own subtitle. Null when no number was shown. Compare with membersRead to see whether the list was fully loaded.

## FAQ

### What does "Telegram — List a group's members" do?

List the members of a Telegram group, each with their user id, display name, role label and presence, read from the group's own info panel. Returns the member total Telegram reports alongside the rows actually read, so a partially loaded list is visible rather than silently short. Refuses a conversation that exposes no member list at all, which is what a broadcast channel does for anyone who is not an admin. Note that opening the conversation marks it read.

### How do I automatically list a group's members on web.telegram.org?

Ask an AI agent connected to Reduck to run reduck/web.telegram.org/get_group_members, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/web.telegram.org/get_group_members

### Is there a web.telegram.org API to list a group's members?

You do not need one. "Telegram — List a group's members" drives the real web.telegram.org pages in a browser, so it works whether or not web.telegram.org offers an API for this.

### What information do I need to provide?

Required: peerId.

### What does it return?

It returns peerId, members, complete, chatTitle, membersRead, membersCount, verified_on_page.

### Do I need to be logged in to web.telegram.org?

Yes. It acts as you on web.telegram.org: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the web.telegram.org cookies saved by the Reduck extension.

### Does it change anything on web.telegram.org, or only read data?

It only reads. It looks things up on web.telegram.org and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/web.telegram.org/get_group_members, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/web.telegram.org/get_group_members

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/web.telegram.org/get_group_members
