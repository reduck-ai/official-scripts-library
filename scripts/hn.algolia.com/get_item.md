# Get a Hacker News item from HN Search by Algolia

Automatically get a Hacker News item from HN Search by Algolia on hn.algolia.com. Read one Hacker News story, comment, job or poll by its id from HN Search (hn.algolia.com): type, title, link, author, points, creation time, text, parent and story ids, its Hacker News item link, and the ids of its direct child comments with their count. Get ids from hn.algolia.com/search. An id with no item gives an error that says so.

- Site: hn.algolia.com
- Address: `reduck/hn.algolia.com/get_item`
- Updated: 2026-11-27 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/hn.algolia.com/get_item`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/hn.algolia.com/get_item
```

## Input

- `id` (string, required): The Hacker News item id, e.g. "8863", or its item link, e.g. https://news.ycombinator.com/item?id=8863.

## Output

- `id` (string, required)
- `hnUrl` (string, required)
- `childIds` (array, required): Ids of the direct child comments, in the site's order.
- `url` (string | null, optional)
- `text` (string | null, optional): The item text, as HTML. Null for a link story with no text.
- `type` (string | null, optional): story, comment, poll, pollopt or job, as the site gives it.
- `title` (string | null, optional)
- `author` (string | null, optional)
- `points` (integer | null, optional)
- `storyId` (string | null, optional)
- `parentId` (string | null, optional)
- `createdAt` (string | null, optional)
- `optionIds` (array, optional): Ids of a poll's options.
- `childCount` (integer, optional)

## FAQ

### What does "Get a Hacker News item from HN Search by Algolia" do?

Read one Hacker News story, comment, job or poll by its id from HN Search (hn.algolia.com): type, title, link, author, points, creation time, text, parent and story ids, its Hacker News item link, and the ids of its direct child comments with their count. Get ids from hn.algolia.com/search. An id with no item gives an error that says so.

### How do I automatically get a Hacker News item from HN Search by Algolia on hn.algolia.com?

Ask an AI agent connected to Reduck to run reduck/hn.algolia.com/get_item, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/hn.algolia.com/get_item

### Is there a hn.algolia.com API to get a Hacker News item from HN Search by Algolia?

You do not need one. "Get a Hacker News item from HN Search by Algolia" drives the real hn.algolia.com pages in a browser, so it works whether or not hn.algolia.com offers an API for this.

### What information do I need to provide?

Required: id.

### What does it return?

It returns id, url, text, type, hnUrl, title, author, points, storyId, childIds, parentId, createdAt, optionIds, childCount.

### Do I need to be logged in to hn.algolia.com?

No. It only uses pages of hn.algolia.com that are reachable without signing in.

### Does it change anything on hn.algolia.com, or only read data?

It only reads. It looks things up on hn.algolia.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/hn.algolia.com/get_item, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/hn.algolia.com/get_item

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/hn.algolia.com/get_item
