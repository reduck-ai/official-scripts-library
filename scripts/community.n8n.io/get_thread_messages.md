# Get n8n Community forum thread messages

Automatically get n8n Community forum thread messages on community.n8n.io. Read one n8n Community forum thread (community.n8n.io) by its id or url: the thread's title, category, tags, author, dates, views, likes, post count, closed and archived state and accepted answer, and its messages (posts) in thread order, 20 per page. Each message has its post number, url, author username and display name, creation and edit dates, the post it replies to, its like count, whether it is the accepted answer, and its text as Markdown (code blocks, links, images and quotes kept). Moderator actions (a thread closed, pinned, moved) are messages with an `action` code and no text. Pass `page` to read further: nextPage is null on the last page, and a page past the end returns no messages. A thread that does not exist, or is private or deleted, fails with a clear message.

- Site: community.n8n.io
- Address: `reduck/community.n8n.io/get_thread_messages`
- Updated: 2026-10-31 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/community.n8n.io/get_thread_messages`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/community.n8n.io/get_thread_messages
```

## Input

- `thread` (string, required): The thread's id ("10789") or its url (https://community.n8n.io/t/<slug>/<id>), as community.n8n.io/get_category_threads returns them.
- `page` (integer, optional): Page of 20 messages, in thread order.

## Output

- `id` (integer, required)
- `url` (string, required)
- `page` (integer, required)
- `posts` (array, required)
- `title` (string, required)
- `nextPage` (integer | null, required)
- `totalPages` (integer, required)
- `tags` (array, optional)
- `views` (integer, optional)
- `author` (string | null, optional)
- `closed` (boolean, optional)
- `archived` (boolean, optional)
- `createdAt` (string, optional)
- `likeCount` (integer, optional)
- `categoryId` (integer, optional)
- `postsCount` (integer, optional): Messages in the thread, the opening post included.
- `lastPostedAt` (string | null, optional)
- `acceptedAnswerPostNumbers` (array, optional)

## FAQ

### What does "Get n8n Community forum thread messages" do?

Read one n8n Community forum thread (community.n8n.io) by its id or url: the thread's title, category, tags, author, dates, views, likes, post count, closed and archived state and accepted answer, and its messages (posts) in thread order, 20 per page. Each message has its post number, url, author username and display name, creation and edit dates, the post it replies to, its like count, whether it is the accepted answer, and its text as Markdown (code blocks, links, images and quotes kept). Moderator actions (a thread closed, pinned, moved) are messages with an `action` code and no text. Pass `page` to read further: nextPage is null on the last page, and a page past the end returns no messages. A thread that does not exist, or is private or deleted, fails with a clear message.

### How do I automatically get n8n Community forum thread messages on community.n8n.io?

Ask an AI agent connected to Reduck to run reduck/community.n8n.io/get_thread_messages, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/community.n8n.io/get_thread_messages

### Is there a community.n8n.io API to get n8n Community forum thread messages?

You do not need one. "Get n8n Community forum thread messages" drives the real community.n8n.io pages in a browser, so it works whether or not community.n8n.io offers an API for this.

### What information do I need to provide?

Required: thread. Optional: page.

### What does it return?

It returns id, url, page, tags, posts, title, views, author, closed, archived, nextPage, createdAt, likeCount, categoryId, postsCount, totalPages, lastPostedAt, acceptedAnswerPostNumbers.

### Do I need to be logged in to community.n8n.io?

No. It only uses pages of community.n8n.io that are reachable without signing in.

### Does it change anything on community.n8n.io, or only read data?

It only reads. It looks things up on community.n8n.io and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/community.n8n.io/get_thread_messages, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/community.n8n.io/get_thread_messages

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/community.n8n.io/get_thread_messages
