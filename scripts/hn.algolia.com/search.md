# Search Hacker News with HN Search by Algolia

Automatically search Hacker News with HN Search by Algolia on hn.algolia.com. Search Hacker News stories and comments with HN Search (hn.algolia.com) and return one page of hits, 30 by default, with each hit's id, type, title, link, author, points, comment count, creation time, text and its Hacker News item link, plus the total hit count and page count. Filter by type (all, story, comment, Ask HN, Show HN, Launch HN, job, poll), sort by popularity or by date, and limit to a date range: a preset or your own start and end dates. Pages start at 0. A search with no match returns an empty list. For a comment, title and link are those of its story.

- Site: hn.algolia.com
- Address: `reduck/hn.algolia.com/search`
- Updated: 2026-11-27 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/hn.algolia.com/search`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/hn.algolia.com/search
```

## Input

- `query` (string, required): Search text, e.g. "browser automation". An empty text lists all items in the order chosen.
- `page` (integer, optional): Result page, from 0.
- `sort` (string, optional): byPopularity or byDate (newest first).
- `type` (string, optional): Kind of item to search.
- `prefix` (boolean, optional): Also match words that start with the last search word. Omit to keep the site's setting.
- `dateEnd` (string, optional): Last day of a custom window, YYYY-MM-DD (UTC), included.
- `dateRange` (string, optional): Time window. Giving dateStart or dateEnd sets it to custom.
- `dateStart` (string, optional): First day of a custom window, YYYY-MM-DD (UTC).

## Output

- `url` (string, required): The HN Search page for this search.
- `hits` (array, required)
- `page` (integer, required)
- `nbHits` (integer, optional): Total number of matching items.
- `nbPages` (integer, optional)
- `hitsPerPage` (integer, optional)

## FAQ

### What does "Search Hacker News with HN Search by Algolia" do?

Search Hacker News stories and comments with HN Search (hn.algolia.com) and return one page of hits, 30 by default, with each hit's id, type, title, link, author, points, comment count, creation time, text and its Hacker News item link, plus the total hit count and page count. Filter by type (all, story, comment, Ask HN, Show HN, Launch HN, job, poll), sort by popularity or by date, and limit to a date range: a preset or your own start and end dates. Pages start at 0. A search with no match returns an empty list. For a comment, title and link are those of its story.

### How do I automatically search Hacker News with HN Search by Algolia on hn.algolia.com?

Ask an AI agent connected to Reduck to run reduck/hn.algolia.com/search, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/hn.algolia.com/search

### Is there a hn.algolia.com API to search Hacker News with HN Search by Algolia?

You do not need one. "Search Hacker News with HN Search by Algolia" drives the real hn.algolia.com pages in a browser, so it works whether or not hn.algolia.com offers an API for this.

### What information do I need to provide?

Required: query. Optional: page, sort, type, prefix, dateEnd, dateRange, dateStart.

### What does it return?

It returns url, hits, page, nbHits, nbPages, hitsPerPage.

### Do I need to be logged in to hn.algolia.com?

No. It only uses pages of hn.algolia.com that are reachable without signing in.

### Does it change anything on hn.algolia.com, or only read data?

It only reads. It looks things up on hn.algolia.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/hn.algolia.com/search, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/hn.algolia.com/search

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/hn.algolia.com/search
