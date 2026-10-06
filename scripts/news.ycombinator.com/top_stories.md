# Top Hacker News stories

You get all 30 front-page stories ranked as on the site, with points and comment counts.

- Site: news.ycombinator.com
- Address: `reduck/news.ycombinator.com/top_stories`
- Updated: 2026-10-05 (v3)
- Author: Reduck AI (reduck)

## About

One run is a snapshot of the Hacker News front page. The official Firebase API has the same list only as bare ids, so that snapshot costs 31 requests there (one for the ids, one per story). Say you posted a Show HN at 8am Pacific: run this every 15 minutes, pick your post out by the item id at the end of comments_url rather than the title, and log rank and points into a sheet. The catch is the start. Every Show HN begins on shownew, and this sees yours only once it reaches the front page. Past rank 30 it drops out again, since page 2 is never loaded. Ask HN posts have no outside link, so url repeats comments_url, and YC job ads carry null points, which makes them easy to drop. Author and age are not captured, so one snapshot cannot tell a fresh story from a slow climber.

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/news.ycombinator.com/top_stories`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/news.ycombinator.com/top_stories
```

## Input

- `n` (integer, optional)

## FAQ

### What does "Top Hacker News stories" do?

Read the top N stories from the Hacker News front page: rank, title, url, points, comments_count and a link to the discussion. The front page lists about 30 stories, so an n above that caps out rather than paginating. A story nobody has commented on yet reports 0 comments; YC job posts carry neither a score nor a discussion, so their points and comments_count are null. If Hacker News is throttling requests from your address, the script says so instead of returning a partial list.

### What information do I need to provide?

Optional: n.

### Do I need to be logged in to news.ycombinator.com?

No. It only uses pages of news.ycombinator.com that are reachable without signing in.

### Does it change anything on news.ycombinator.com, or only read data?

It only reads. It looks things up on news.ycombinator.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/news.ycombinator.com/top_stories, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/news.ycombinator.com/top_stories

### Who maintains it?

It is part of Reduck's official curated catalogue.

### Can I get more than 30 Hacker News stories, or page 2?

Top Hacker News stories loads the front page of news.ycombinator.com once and stops there, so an n of 50 returns the same 30 stories as an n of 30. For a deeper list, the official Firebase API's /v0/topstories endpoint gives up to 500 ids (jobs included), but each id needs its own /v0/item/<id>.json request before you have a title or a score.

### Can it read Show HN, Ask HN, newest or best instead of the front page?

This script loads only the main front page at news.ycombinator.com, so Show HN, Ask HN, newest and best are out of its reach, and a fresh Show HN appears here only once it climbs onto that page. The official Firebase API lists those feeds as ids: up to 500 at /v0/newstories, best stories at /v0/beststories, and up to 200 each at /v0/askstories and /v0/showstories.

### Does the Algolia Hacker News search API give the same order as the front page?

Hacker News Search by Algolia, queried with tags=front_page on 5 October 2026, returned the front-page set (one check found it a story behind the live page) sorted by points, not by on-site rank. Its hits do carry author, created_at and objectID, which this output lacks, and objectID matches the id at the end of comments_url, so the two join cleanly. The ids from the official Firebase /v0/topstories endpoint matched the page's order in the same checks, give or take one swapped pair.

### What happens if Hacker News refuses to serve the front page?

When Hacker News answers with its "not able to serve your requests" or "too many requests" notice and no stories, the run stops with an error instead of handing back an empty array you might log as a quiet hour. The error message suggests waiting a minute before trying again.

Source: https://reduck.ai/explore/scripts/reduck/news.ycombinator.com/top_stories
