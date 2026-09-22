# Unblock a TikTok user

Automatically unblock a TikTok user on tiktok.com. Unblock a TikTok account by @username, as the signed-in account. Safe to repeat: if the account is not blocked nothing is sent and the run says so. Unblocking does not restore a follow relationship that blocking removed. The run reports the state TikTok holds afterwards, and the companion block script is the reverse.

- Site: tiktok.com
- Address: `reduck/tiktok.com/unblock_user`
- Updated: 2026-09-03 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/tiktok.com/unblock_user`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/tiktok.com/unblock_user
```

## Input

- `username` (string, required): TikTok handle to unblock, with or without a leading @ (e.g. "tiktok" or "@tiktok").

## Output

- `userId` (string, required)
- `blocked` (boolean, required): Whether the account is still blocked at the end of the run; false on success.
- `username` (string, required): Handle as TikTok reports it for the account that was acted on.
- `already_unblocked` (boolean, required): True when it was not blocked before this run, so nothing was sent.
- `nickname` (string | null, optional)
- `verified` (boolean | null, optional): True when a fresh read of the relationship confirmed the block is gone. Null when TikTok would not report the relationship, in which case the result rests on the response to the unblock itself.
- `account_used` (string | null, optional): Handle that performed the unblock, read from the signed-in session rather than assumed.
- `blocked_by_them` (boolean | null, optional): Whether that account has blocked you, as far as TikTok will say.

## FAQ

### What does "Unblock a TikTok user" do?

Unblock a TikTok account by @username, as the signed-in account. Safe to repeat: if the account is not blocked nothing is sent and the run says so. Unblocking does not restore a follow relationship that blocking removed. The run reports the state TikTok holds afterwards, and the companion block script is the reverse.

### How do I automatically unblock a TikTok user on tiktok.com?

Ask an AI agent connected to Reduck to run reduck/tiktok.com/unblock_user, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/tiktok.com/unblock_user

### Is there a tiktok.com API to unblock a TikTok user?

You do not need one. "Unblock a TikTok user" drives the real tiktok.com pages in a browser, so it works whether or not tiktok.com offers an API for this.

### What information do I need to provide?

Required: username.

### What does it return?

It returns userId, blocked, nickname, username, verified, account_used, blocked_by_them, already_unblocked.

### Do I need to be logged in to tiktok.com?

Yes. It acts as you on tiktok.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the tiktok.com cookies saved by the Reduck extension.

### Does it change anything on tiktok.com, or only read data?

It makes changes on tiktok.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/tiktok.com/unblock_user, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/tiktok.com/unblock_user

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/tiktok.com/unblock_user
