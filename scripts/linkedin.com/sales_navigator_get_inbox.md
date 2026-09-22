# Sales Navigator – Get inbox

Automatically get inbox on linkedin.com. List the latest LinkedIn Sales Navigator inbox conversations. Args: count (page size), filter (the inbox folder: INBOX default, UNREAD, ARCHIVED), and pageStartsAt for pagination. Paginate newest to oldest by passing the returned nextPageStartsAt as pageStartsAt. Needs a Sales Navigator seat. Returns the viewer identity and threads (threadId, unread/unreadCount, archived, totalMessageCount, the other participants with salesLeadUrl, and the last message with body/subject/type/deliveredAt and direction).

- Site: linkedin.com
- Address: `reduck/linkedin.com/sales_navigator_get_inbox`
- Updated: 2026-09-03 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/linkedin.com/sales_navigator_get_inbox`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/linkedin.com/sales_navigator_get_inbox
```

## Input

- `count` (integer, optional): Threads per page. Default 20.
- `filter` (string, optional): Inbox folder, mapping to the 'All messages' dropdown. Observed values: INBOX (default, all conversations), UNREAD, ARCHIVED.
- `pageStartsAt` (integer, optional): Time cursor in ms epoch for pagination (newest→oldest). Omit for the newest page; to fetch older threads pass the nextPageStartsAt returned by the previous call. Time-based, so stable under replay.

## Output

- `count` (integer, required)
- `filter` (string, required)
- `threads` (array, required)
- `total` (integer | null, optional): Total threads in this folder.
- `viewerUrn` (string | null, optional)
- `viewerName` (string | null, optional)
- `nextPageStartsAt` (integer | null, optional): Cursor for the next (older) page; pass back as pageStartsAt. null when the page is empty.

## FAQ

### What does "Sales Navigator – Get inbox" do?

List the latest LinkedIn Sales Navigator inbox conversations. Args: count (page size), filter (the inbox folder: INBOX default, UNREAD, ARCHIVED), and pageStartsAt for pagination. Paginate newest to oldest by passing the returned nextPageStartsAt as pageStartsAt. Needs a Sales Navigator seat. Returns the viewer identity and threads (threadId, unread/unreadCount, archived, totalMessageCount, the other participants with salesLeadUrl, and the last message with body/subject/type/deliveredAt and direction).

### How do I automatically get inbox on linkedin.com?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/sales_navigator_get_inbox, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/sales_navigator_get_inbox

### Is there a linkedin.com API to get inbox?

You do not need one. "Sales Navigator – Get inbox" drives the real linkedin.com pages in a browser, so it works whether or not linkedin.com offers an API for this.

### What information do I need to provide?

Optional: count, filter, pageStartsAt.

### What does it return?

It returns count, total, filter, threads, viewerUrn, viewerName, nextPageStartsAt.

### Do I need to be logged in to linkedin.com?

Yes. It acts as you on linkedin.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the linkedin.com cookies saved by the Reduck extension.

### Does it change anything on linkedin.com, or only read data?

Unknown: its author has not declared whether it changes anything on linkedin.com, so treat it as if it could.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/sales_navigator_get_inbox, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/sales_navigator_get_inbox

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/linkedin.com/sales_navigator_get_inbox
