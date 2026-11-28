# Reset Muse (muse.ai)

Automatically reset Muse (muse.ai) on muse.ai. Reset the signed-in Muse account (Meta's personal agent at muse.ai) to a new account's state: the same reset as Muse's own Settings > Data controls > Reset Muse. Muse permanently deletes all its data: every chat and its history, its memory (MEMORY.md, the daily notes, the nightly profile of the user), files, spaces and active tasks, and starts again with an empty memory, its default scheduled tasks and a welcome message in the main chat. Only the user's name, which Muse takes from the Meta account, stays. Use it for a clean slate, for example before an eval: deleting memory files is not enough, as Muse also recalls from its past chats. After a reset, Muse's memory files are its empty templates (MEMORY.md with its headings only, near-empty banks under memory/bank/), and Muse can add empty indexes such as memory/people/INDEX.md: they hold nothing about the user. Their modifiedAt can be older than the reset, so check a reset by the chats (only the main chat left) or by reading the files, not by their dates. This cannot be undone: pass confirm: true to run it. The run returns once the new account is ready to answer, with how many chats there were before and after. A run that fails after it started can still have reset the account: check with muse.ai/list_chats (only the main chat left) before you run it again. Run Muse scripts one at a time: Muse lets only a few browser tabs hold an account's connection. Requires a signed-in session: a signed-out browser fails at once with an error that says so.

- Site: muse.ai
- Address: `reduck/muse.ai/reset_muse`
- Updated: 2026-11-27 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/muse.ai/reset_muse`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/muse.ai/reset_muse
```

## Input

- `confirm` (any, required): Must be true. Everything Muse holds is deleted and cannot be recovered.

## Output

- `resetAt` (string, required): When Muse accepted the reset, ISO 8601.
- `chatsAfter` (integer, required): How many it has after the reset: 1 (the main chat) or 0 while Muse writes its welcome.
- `chatsBefore` (integer, required): How many chats the account had, the main chat included.

## FAQ

### What does "Reset Muse (muse.ai)" do?

Reset the signed-in Muse account (Meta's personal agent at muse.ai) to a new account's state: the same reset as Muse's own Settings > Data controls > Reset Muse. Muse permanently deletes all its data: every chat and its history, its memory (MEMORY.md, the daily notes, the nightly profile of the user), files, spaces and active tasks, and starts again with an empty memory, its default scheduled tasks and a welcome message in the main chat. Only the user's name, which Muse takes from the Meta account, stays. Use it for a clean slate, for example before an eval: deleting memory files is not enough, as Muse also recalls from its past chats. After a reset, Muse's memory files are its empty templates (MEMORY.md with its headings only, near-empty banks under memory/bank/), and Muse can add empty indexes such as memory/people/INDEX.md: they hold nothing about the user. Their modifiedAt can be older than the reset, so check a reset by the chats (only the main chat left) or by reading the files, not by their dates. This cannot be undone: pass confirm: true to run it. The run returns once the new account is ready to answer, with how many chats there were before and after. A run that fails after it started can still have reset the account: check with muse.ai/list_chats (only the main chat left) before you run it again. Run Muse scripts one at a time: Muse lets only a few browser tabs hold an account's connection. Requires a signed-in session: a signed-out browser fails at once with an error that says so.

### How do I automatically reset Muse (muse.ai) on muse.ai?

Ask an AI agent connected to Reduck to run reduck/muse.ai/reset_muse, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/muse.ai/reset_muse

### Is there a muse.ai API to reset Muse (muse.ai)?

You do not need one. "Reset Muse (muse.ai)" drives the real muse.ai pages in a browser, so it works whether or not muse.ai offers an API for this.

### What information do I need to provide?

Required: confirm.

### What does it return?

It returns resetAt, chatsAfter, chatsBefore.

### Do I need to be logged in to muse.ai?

Yes. It acts as you on muse.ai: in your browser it reuses your session, and on a cloud browser it loads your Auth session cookies for muse.ai.

### Does it change anything on muse.ai, or only read data?

It makes changes on muse.ai, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/muse.ai/reset_muse, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/muse.ai/reset_muse

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/muse.ai/reset_muse
