# get_member_list

Member names, user ids and a bot flag from a Discord channel's sidebar, up to the limit you set.

- Site: discord.com
- Address: `reduck/discord.com/get_member_list`
- Updated: 2026-10-05 (v12)
- Author: Reduck AI (reduck)

## About

Most useful for moderators of small and mid-size servers. Paste the URL of a text channel such as #mod-chat and you get the names the member sidebar lists for it, which means only people who can read that channel. A channel might return 14 rows, two flagged isApp. Compare them against your real mod roster. Leftovers tend to be a helper whose role never got removed, or a bot nobody remembers adding. Names are what the sidebar shows, the server nickname rather than the @username, and role headings are not kept. The userId comes from the avatar URL, so it can be null, for default avatars and possibly others. Big servers are where it falls short. The sidebar is scrolled at most 40 times, half a screen each, and Discord may leave offline members out, so you can end up with online people only. The official route to a full roster is a bot with the GUILD_MEMBERS intent.

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/discord.com/get_member_list`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/discord.com/get_member_list
```

## Input

- `channelUrl` (string, required): URL of a text channel in the server, e.g. https://discord.com/channels/<guildId>/<channelId>. The member sidebar belongs to the channel, so it must be one the account can view.
- `limit` (integer, optional): How many members to return.

## Output

- `count` (integer, required)
- `members` (array, required)
- `guildId` (string | null, optional)
- `complete` (boolean, optional): True when the full member list was read before limit was reached. On large servers Discord does not show every member at once, so fewer may be returned than the server holds.

## Example output

Shape only: placeholder values generated from the output schema, not a real run.

```json
{
  "count": 3,
  "guildId": "abc123",
  "members": [
    {
      "name": "Example",
      "isApp": true,
      "userId": "abc123"
    }
  ],
  "complete": true
}
```

## FAQ

### What does "get_member_list" do?

List the members of a Discord server, as shown in the member list for a given channel. Returns each member's userId, display name, and whether Discord marks them as an app or bot. userId is null for members using a default avatar. On large servers Discord does not show every member at once, so the result may not be the full roster; complete tells you whether it was. Offline members may be left out, and role groupings are not returned.

### What information do I need to provide?

Required: channelUrl. Optional: limit.

### What does it return?

It returns count, guildId, members, complete.

### Do I need to be logged in to discord.com?

Yes. It acts as you on discord.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the discord.com cookies saved by the Reduck extension.

### Does it change anything on discord.com, or only read data?

It only reads. It looks things up on discord.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/discord.com/get_member_list, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/discord.com/get_member_list

### Who maintains it?

It is part of Reduck's official curated catalogue.

### How many members can one run return?

A few hundred at most. limit defaults to 100 and has no ceiling, but the sidebar is scrolled only 40 times, half a screen each, so the exact figure depends on window height. If count is below your limit, complete can still read true when that scroll cap stopped the run, so it does not prove you got everyone. Compare count with the member total Discord shows.

### Does it give me @usernames or roles?

No. Each row has the name the sidebar displays, which is the server nickname or display name rather than the @username. The role headings the sidebar groups people under are not kept, and neither are join dates.

### Why are some people missing from the result?

The sidebar belongs to the channel you pass, so it lists only members who can view that channel. On large servers Discord may also leave offline members out. Voice channels have no member sidebar, and the run stops with an error.

Source: https://reduck.ai/explore/scripts/reduck/discord.com/get_member_list
