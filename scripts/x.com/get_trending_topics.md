# Get X trending topics

Automatically get X trending topics on x.com. Read X's Explore trends for a given tab (trending, news, sports, entertainment or for-you), with each trend's rank, name, context line and post count where shown. Results are personalised to the logged-in account's location and interests, not a global chart.

- Site: x.com
- Address: `reduck/x.com/get_trending_topics`
- Updated: 2026-09-03 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/x.com/get_trending_topics`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/x.com/get_trending_topics
```

## Input

- `tab` (string, optional): Which Explore tab to read. "trending" returns ranked topics (rank + "Music · Trending" + name), while news, sports and entertainment return headline stories (headline + "9 hours ago · Other · 195K posts"). "for_you" mixes the two shapes in one list, so expect some rows with a rank and some without.
- `limit` (integer, optional): Maximum entries to return, in the order X ranks them. The trending tab renders about 30 without scrolling and the topical tabs far fewer — sports returned only 5 — so asking for more scrolls until the list stops growing and simply returns what the tab holds.

## Output

- `tab` (string, required)
- `url` (string, required): The Explore tab URL actually read.
- `count` (integer, required)
- `trends` (array, required)
- `note` (string | null, optional): Set when a tab rendered no rows at all — normal for for_you, which is a timeline rather than a list.

## FAQ

### What does "Get X trending topics" do?

Read X's Explore trends for a given tab (trending, news, sports, entertainment or for-you), with each trend's rank, name, context line and post count where shown. Results are personalised to the logged-in account's location and interests, not a global chart.

### How do I automatically get X trending topics on x.com?

Ask an AI agent connected to Reduck to run reduck/x.com/get_trending_topics, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/x.com/get_trending_topics

### Is there a x.com API to get X trending topics?

You do not need one. "Get X trending topics" drives the real x.com pages in a browser, so it works whether or not x.com offers an API for this.

### What information do I need to provide?

Optional: tab, limit.

### What does it return?

It returns tab, url, note, count, trends.

### Do I need to be logged in to x.com?

Yes. It acts as you on x.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the x.com cookies saved by the Reduck extension.

### Does it change anything on x.com, or only read data?

It only reads. It looks things up on x.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/x.com/get_trending_topics, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/x.com/get_trending_topics

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/x.com/get_trending_topics
