# Find Discord member ID by name

Automatically find Discord member ID by name on discord.com. Get the numeric user ID, plus anyone with a similar name, so a message pings the right person.

- Site: discord.com
- Address: `reduck/discord.com/find_member_id`
- Updated: 2026-10-05 (v14)
- Author: Reduck AI (reduck)

## About

Discord hides user IDs until you turn on Developer Mode (User Settings > Advanced) and right-click someone to copy theirs. Fine for one person. An agent posting for you has it harder, because a real mention must be written as <@userId>. You pass a name, or the start of one, and the link to a channel in that person's server. The lookup types @name into that channel's message box, reads the IDs off the mention popup and clears the box without sending. Say a moderator's agent is posting the Friday scrim lineup. It passes "marta" with the #general link, gets her ID plus any other Martas in matches, and checks the label before writing <@userId>. A bot can run a similar prefix search on usernames and nicknames through Discord's Search Guild Members endpoint, once someone with Manage Server adds it. The catch is that you must be signed in, and only members of that channel's server show up.

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/discord.com/find_member_id`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/discord.com/find_member_id
```

## Input

- `name` (string, required): Name (or start of the name) of the member to resolve. Throws when no member matches.
- `channelUrl` (string, required): URL of a channel in the server to search, e.g. https://discord.com/channels/<guildId>/<channelId>. Must be a channel the signed-in account can type in (the lookup runs through that channel's message box).

## Output

- `userId` (string | null, required): userId of the first result (best match), or null.
- `matches` (array, required): All members offered by the autocomplete, best first.

## Example output

Shape only: placeholder values generated from the output schema, not a real run.

```json
{
  "userId": "abc123",
  "matches": [
    {
      "label": "Example",
      "userId": "abc123"
    }
  ]
}
```

## FAQ

### What does "Find Discord member ID by name" do?

Resolves a Discord member's userId from their name, through a channel's mention autocomplete (@name). Useful to build a <@id> ping. Requires being logged in.

### How do I automatically find Discord member ID by name on discord.com?

Ask an AI agent connected to Reduck to run reduck/discord.com/find_member_id, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/discord.com/find_member_id

### Is there a discord.com API to find Discord member ID by name?

You do not need one. "Find Discord member ID by name" drives the real discord.com pages in a browser, so it works whether or not discord.com offers an API for this.

### What information do I need to provide?

Required: channelUrl, name.

### What does it return?

It returns userId, matches.

### Do I need to be logged in to discord.com?

Yes. It acts as you on discord.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the discord.com cookies saved by the Reduck extension.

### Does it change anything on discord.com, or only read data?

It only reads. It looks things up on discord.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/discord.com/find_member_id, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/discord.com/find_member_id

### Who maintains it?

It is part of Reduck's official curated catalogue.

### Can I look up a Discord profile from a user ID?

No, this lookup only goes from a name to an ID. If you are signed in to Discord, opening discord.com/users/<id> in your browser shows that person's profile. With a bot token, Discord's official GET /users/{user.id} endpoint returns the user object for a given ID.

### What if a lot of people in the server share the same first name?

You get the members Discord's @ popup showed, best first, and userId is only the top one, so check the label before pinging anyone. A two-word name like "marta lopez" is typed as "@marta" and then filtered to labels containing the whole name, so in a server full of Martas she can fall outside the popup and the run fails instead of returning someone else. Passing her username usually narrows it down, since Discord usernames have no spaces and the @ search matches them too.

### Which channel link should I pass in?

Pick a regular text channel where you have no unsent draft, because the lookup empties that channel's message box before typing and again afterwards, so a half-written message there is lost. Read-only channels, such as an announcement channel you cannot post in, have no box to type in, and the run stops with a "message box never appeared" error.

### Does it find members who still use the default Discord avatar?

Yes. With a default avatar the ID is not in the image URL, so the lookup reads it from the popup row itself. The get_member_list script, which reads the server's member sidebar, returns userId null for those members and may not show everyone on a large server, so this lookup is the better pick once you know who you want.

Source: https://reduck.ai/explore/scripts/reduck/discord.com/find_member_id
