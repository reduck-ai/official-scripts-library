# Get n8n Community forum category threads

Automatically get n8n Community forum category threads on community.n8n.io. List the threads (topics) of one n8n Community forum category (community.n8n.io), one page at a time, with the forum's own sorts: latest, hot, or top over a period, optionally ordered by a column (views, posts, likes, created, activity) and filtered by a tag. A parent category also lists its subcategories' threads, each with its own categoryId. Returns per thread its id, title, url, categoryId, author, last poster, creation and last post dates, post count (the opening post included), views, likes, tags, pinned, closed, archived, whether it has an accepted answer, and the excerpt the forum shows (pinned threads only). Pages hold 30 threads (50 for top); nextPage is null on the last page, and a page past the end returns no threads. Pass a thread's id or url to community.n8n.io/get_thread_messages to read it. An unknown category or tag fails with a clear message: get category ids from community.n8n.io/list_categories.

- Site: community.n8n.io
- Address: `reduck/community.n8n.io/get_category_threads`
- Updated: 2026-10-31 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/community.n8n.io/get_category_threads`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/community.n8n.io/get_category_threads
```

## Input

- `category` (string, required): The category's id ("15"), its url (https://community.n8n.io/c/built-with-n8n/15) or its slug path ("built-with-n8n", "feature-requests/nodes"), as community.n8n.io/list_categories returns them.
- `tag` (string, optional): Only threads with this tag, e.g. "ai".
- `page` (integer, optional)
- `sort` (string, optional): latest: most recent activity first, pinned threads at the top. hot: trending now. top: most active over `period`.
- `order` (string, optional): Order the list by this column instead of the sort's own order, as clicking a column header does.
- `period` (string, optional): Time window of the top sort. Ignored by the other sorts.
- `ascending` (boolean, optional): With `order`: smallest first.

## Output

- `page` (integer, required)
- `topics` (array, required)
- `nextPage` (integer | null, required)

## FAQ

### What does "Get n8n Community forum category threads" do?

List the threads (topics) of one n8n Community forum category (community.n8n.io), one page at a time, with the forum's own sorts: latest, hot, or top over a period, optionally ordered by a column (views, posts, likes, created, activity) and filtered by a tag. A parent category also lists its subcategories' threads, each with its own categoryId. Returns per thread its id, title, url, categoryId, author, last poster, creation and last post dates, post count (the opening post included), views, likes, tags, pinned, closed, archived, whether it has an accepted answer, and the excerpt the forum shows (pinned threads only). Pages hold 30 threads (50 for top); nextPage is null on the last page, and a page past the end returns no threads. Pass a thread's id or url to community.n8n.io/get_thread_messages to read it. An unknown category or tag fails with a clear message: get category ids from community.n8n.io/list_categories.

### How do I automatically get n8n Community forum category threads on community.n8n.io?

Ask an AI agent connected to Reduck to run reduck/community.n8n.io/get_category_threads, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/community.n8n.io/get_category_threads

### Is there a community.n8n.io API to get n8n Community forum category threads?

You do not need one. "Get n8n Community forum category threads" drives the real community.n8n.io pages in a browser, so it works whether or not community.n8n.io offers an API for this.

### What information do I need to provide?

Required: category. Optional: tag, page, sort, order, period, ascending.

### What does it return?

It returns page, topics, nextPage.

### Do I need to be logged in to community.n8n.io?

No. It only uses pages of community.n8n.io that are reachable without signing in.

### Does it change anything on community.n8n.io, or only read data?

It only reads. It looks things up on community.n8n.io and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/community.n8n.io/get_category_threads, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/community.n8n.io/get_category_threads

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/community.n8n.io/get_category_threads
