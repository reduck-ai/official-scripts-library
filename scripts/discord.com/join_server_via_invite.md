# join_server_via_invite

Join a Discord server using an invite link or code, e.g. https://discord.com/invite/<code> or just the code. Returns the server's id and name, and whether the account was already a member before this ran. This is a write with lasting effect: joining a server is visible to its members and puts you on its member list until you leave.

- Site: discord.com
- Address: `reduck/discord.com/join_server_via_invite`
- Updated: 2026-09-03 (v16)
- Author: Reduck AI (reduck)

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

It makes changes on discord.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/discord.com/join_server_via_invite, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/discord.com/join_server_via_invite

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/discord.com/join_server_via_invite
