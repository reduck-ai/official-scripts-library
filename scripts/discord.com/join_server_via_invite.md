# join_server_via_invite

Your account ends up in the server and you get its ID and name back; a dead invite changes nothing.

- Site: discord.com
- Address: `reduck/discord.com/join_server_via_invite`
- Updated: 2026-10-05 (v20)
- Author: Reduck AI (reduck)

## About

A community manager at a game studio keeps invite links copied from rival games' Steam pages and wants their patch notes. One run takes one link, say discord.gg/7Fq2kXz?utm_source=steam (the tracking part and stray spaces get stripped). Back come guildId and guildName, ready for discord.com/list_channels to find #announcements, then read_messages. Nothing gets clicked until Discord's invite preview confirms the link is live, so an expired invite leaves your account untouched. If your sidebar already lists the server, you get already_member: true and the invite page is never opened. Joining is visible, though. You stay on the member list until you leave or get removed, and many servers post a welcome message with your name. Stay near the browser, since Discord can show a captcha on the join, more often after several joins in a row, and the run stops waiting after 15 seconds. Close your own Discord tabs first, because Discord sometimes allows only one active tab per account.

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/discord.com/join_server_via_invite`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/discord.com/join_server_via_invite
```

## Input

- `invite` (string, required): An invite link (e.g. https://discord.com/invite/abc123 or https://discord.gg/abc123, with or without tracking query params) or a bare invite code (abc123). Surrounding whitespace is tolerated.

## Output

- `joined` (boolean, required)
- `guildId` (string | null, required)
- `guildName` (string | null, required)
- `already_member` (boolean, required)

## Example output

Shape only: placeholder values generated from the output schema, not a real run.

```json
{
  "joined": true,
  "guildId": "abc123",
  "guildName": "…",
  "already_member": true
}
```

## FAQ

### What does "join_server_via_invite" do?

Join a Discord server using an invite link or code, e.g. https://discord.com/invite/<code> or just the code. Returns the server's id and name, and whether the account was already a member before this ran. This is a write with lasting effect: joining a server is visible to its members and puts you on its member list until you leave.

### What information do I need to provide?

Required: invite.

### What does it return?

It returns joined, guildId, guildName, already_member.

### Do I need to be logged in to discord.com?

Yes. It acts as you on discord.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the discord.com cookies saved by the Reduck extension.

### Does it change anything on discord.com, or only read data?

It makes changes on discord.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/discord.com/join_server_via_invite, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/discord.com/join_server_via_invite

### Who maintains it?

It is part of Reduck's official curated catalogue.

### What happens if the Discord invite has expired or the join does not go through?

An expired or revoked invite fails Discord's invite lookup before any button is pressed, so your account stays unchanged. The murkier case is a valid invite that never puts you inside the server within 15 seconds, say an unsolved captcha or a full server: that error says the outcome is unconfirmed, so check discord.com/list_servers before retrying.

### Can I join a Discord server with just its server ID or a user ID?

Joining needs an invite, either a discord.gg or discord.com/invite link or the code at the end of one. A server ID or user ID pasted in is read as an invite code, Discord's invite lookup finds nothing under it, and the run stops with nothing changed. Ask someone already in the server for an invite, or look for one on the server's own website.

### Is there a limit to how many Discord servers one account can join?

Free and Nitro Basic accounts top out at 100 servers and full Nitro at 200, according to Discord's support page on account caps. At the cap the join does not go through, so the run ends with an error instead of joined: true. Leave a server you no longer read and try again.

### Can I post in a Discord server as soon as the join succeeds?

A joined: true result only means the browser reached the server's own URL, not that the account can post yet. On a server with Rules Screening, Discord keeps new members pending and unable to talk or react until they accept the rules, so do that in Discord before running post_message there. Onboarding questions and role pickers are left for you as well.

Source: https://reduck.ai/explore/scripts/reduck/discord.com/join_server_via_invite
