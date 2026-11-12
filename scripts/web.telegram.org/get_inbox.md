# Get Telegram inbox

Automatically get Telegram inbox on web.telegram.org. List the conversations of the Telegram account signed in to this browser, in the order Telegram shows them: each one's peer id (the id the other Telegram scripts take), kind, title, unread and mention counts, and its last message, with a read receipt for a message the account sent. Also returns the account itself. Returns 100 conversations a page: pass nextCursor for the next page, or archived for the archive. Reading does not mark anything as read.

- Site: web.telegram.org
- Address: `reduck/web.telegram.org/get_inbox`
- Updated: 2026-11-11 (v9)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/web.telegram.org/get_inbox`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/web.telegram.org/get_inbox
```

## Input

- `cursor` (string, optional): Omit for the first page. To read the next one, pass the nextCursor of the previous call (with the same archived value).
- `archived` (boolean, optional): True to list the archived conversations instead of the main list.

## Output

- `chats` (array, required): Up to 100 conversations, in the order Telegram lists them: pinned first, then by last activity. Empty when the list has none.
- `account` (object, required): The Telegram account this browser is signed in as: confirm it before anything that writes.
- `nextCursor` (string | null, required): Pass it as cursor to read the next page. Null on the last page.
- `totalCount` (integer | null, optional): How many conversations the list holds in all.

## FAQ

### What does "Get Telegram inbox" do?

List the conversations of the Telegram account signed in to this browser, in the order Telegram shows them: each one's peer id (the id the other Telegram scripts take), kind, title, unread and mention counts, and its last message, with a read receipt for a message the account sent. Also returns the account itself. Returns 100 conversations a page: pass nextCursor for the next page, or archived for the archive. Reading does not mark anything as read.

### How do I automatically get Telegram inbox on web.telegram.org?

Ask an AI agent connected to Reduck to run reduck/web.telegram.org/get_inbox, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/web.telegram.org/get_inbox

### Is there a web.telegram.org API to get Telegram inbox?

You do not need one. "Get Telegram inbox" drives the real web.telegram.org pages in a browser, so it works whether or not web.telegram.org offers an API for this.

### What information do I need to provide?

Optional: cursor, archived.

### What does it return?

It returns chats, account, nextCursor, totalCount.

### Do I need to be logged in to web.telegram.org?

Yes. It acts as you on web.telegram.org: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the web.telegram.org cookies saved by the Reduck extension.

### Does it change anything on web.telegram.org, or only read data?

It only reads. It looks things up on web.telegram.org and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/web.telegram.org/get_inbox, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/web.telegram.org/get_inbox

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/web.telegram.org/get_inbox
