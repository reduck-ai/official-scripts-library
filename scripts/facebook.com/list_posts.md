# Scrape posts from a Facebook group or page

Automatically scrape posts from a Facebook group or page on facebook.com. Scrape posts from a Facebook group or page feed as structured data: author, text, reactions, comments, shares. List posts from a Facebook group or page feed (pass its full URL). Returns per post postId, url, author, authorUrl, reactions, comments, shares, createdTime and text. Counts are the site's displayed strings (e.g. "1,2 k"); the feed is a capped sample (by limit) in the default relevance order, not strict reverse-chronological.

- Site: facebook.com
- Address: `reduck/facebook.com/list_posts`
- Updated: 2026-09-19 (v9)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/facebook.com/list_posts`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/facebook.com/list_posts
```

## Input

- `url` (string, required): Full URL of a Facebook group (https://www.facebook.com/groups/<id>) or page (https://www.facebook.com/<username> or /profile.php?id=<id>).
- `limit` (integer, optional): Max posts to return. The feed loads more as needed until this many unique posts are found or the feed stops yielding new ones.
- `withStatus` (boolean, optional): Group URLs only. When true, return {groupStatus, posts} instead of the bare posts array. groupStatus: joined (membership control or readable member feed), not_member (join button shown), pending (join request sent), unavailable (group deleted, or the session is banned/excluded — Facebook shows the same 'content unavailable' page for both), unknown. With withStatus an unavailable group is a result, not an error.

## FAQ

### What does "Scrape posts from a Facebook group or page" do?

Scrape posts from a Facebook group or page feed as structured data: author, text, reactions, comments, shares. List posts from a Facebook group or page feed (pass its full URL). Returns per post postId, url, author, authorUrl, reactions, comments, shares, createdTime and text. Counts are the site's displayed strings (e.g. "1,2 k"); the feed is a capped sample (by limit) in the default relevance order, not strict reverse-chronological.

### How do I automatically scrape posts from a Facebook group or page on facebook.com?

Ask an AI agent connected to Reduck to run reduck/facebook.com/list_posts, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/facebook.com/list_posts

### Is there a facebook.com API to scrape posts from a Facebook group or page?

You do not need one. "Scrape posts from a Facebook group or page" drives the real facebook.com pages in a browser, so it works whether or not facebook.com offers an API for this.

### What information do I need to provide?

Required: url. Optional: limit, withStatus.

### Do I need to be logged in to facebook.com?

No. It only uses pages of facebook.com that are reachable without signing in.

### Does it change anything on facebook.com, or only read data?

It only reads. It looks things up on facebook.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/facebook.com/list_posts, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/facebook.com/list_posts

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/facebook.com/list_posts
