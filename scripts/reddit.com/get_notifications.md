# Get Reddit notifications

Automatically get Reddit notifications on reddit.com. List the notifications of the signed-in Reddit account, newest first, 20 per page: replies to your posts, replies to your comments, mentions and the other kinds Reddit sends. Each one gives its type, whether it is still unread, who sent it, the subreddit, the link to the reply, its full text and its date. Reading does not mark anything as read or seen. Chat messages are a separate surface (reddit.com/get_inbox). Pass the returned nextCursor as cursor to read the next page; it is null on the last page.

- Site: reddit.com
- Address: `reduck/reddit.com/get_notifications`
- Updated: 2026-11-24 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/reddit.com/get_notifications`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/reddit.com/get_notifications
```

## Input

- `cursor` (string, optional): The nextCursor of the previous answer, to read the next page. Omit for the first page.

## Output

- `nextCursor` (string | null, required): Pass as cursor to read the next page; null on the last page.
- `notifications` (array, required)

## FAQ

### What does "Get Reddit notifications" do?

List the notifications of the signed-in Reddit account, newest first, 20 per page: replies to your posts, replies to your comments, mentions and the other kinds Reddit sends. Each one gives its type, whether it is still unread, who sent it, the subreddit, the link to the reply, its full text and its date. Reading does not mark anything as read or seen. Chat messages are a separate surface (reddit.com/get_inbox). Pass the returned nextCursor as cursor to read the next page; it is null on the last page.

### How do I automatically get Reddit notifications on reddit.com?

Ask an AI agent connected to Reduck to run reduck/reddit.com/get_notifications, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/reddit.com/get_notifications

### Is there a reddit.com API to get Reddit notifications?

You do not need one. "Get Reddit notifications" drives the real reddit.com pages in a browser, so it works whether or not reddit.com offers an API for this.

### What information do I need to provide?

Optional: cursor.

### What does it return?

It returns nextCursor, notifications.

### Do I need to be logged in to reddit.com?

Yes. It acts as you on reddit.com: in your browser it reuses your session, and on a cloud browser it loads your Auth session cookies for reddit.com.

### Does it change anything on reddit.com, or only read data?

It only reads. It looks things up on reddit.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/reddit.com/get_notifications, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/reddit.com/get_notifications

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/reddit.com/get_notifications
