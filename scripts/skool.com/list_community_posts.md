# List community posts

Automatically list community posts on skool.com. List the posts in a Skool community feed, newest first. Returns per post the title, body text, author name and handle, creation time, comment and upvote counts, whether it is pinned, the channel it was posted in, and a direct url. Takes the community slug as it appears in the URL (case-insensitive) and a limit, paging through the feed as needed. Reads the community's server-rendered data, so it makes no extra API calls. Fails with a clear message when the slug does not exist or the community is private to this account, rather than returning an empty list.

- Site: skool.com
- Address: `reduck/skool.com/list_community_posts`
- Updated: 2026-09-17 (v8)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/skool.com/list_community_posts`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/skool.com/list_community_posts
```

## Input

- `group` (string, required): Community slug as it appears in the URL, e.g. "cliefnotes" for https://www.skool.com/cliefnotes. Case-insensitive: Skool slugs are lowercase and the value is normalised.
- `limit` (integer, optional): How many posts to return, newest first.

## Output

- `count` (integer, required)
- `group` (string, required)
- `posts` (array, required)
- `complete` (boolean, required): True when every post in the community was returned (not truncated by limit).
- `totalInCommunity` (integer | null, required): Total posts Skool reports for this community, independent of limit.

## FAQ

### What does "List community posts" do?

List the posts in a Skool community feed, newest first. Returns per post the title, body text, author name and handle, creation time, comment and upvote counts, whether it is pinned, the channel it was posted in, and a direct url. Takes the community slug as it appears in the URL (case-insensitive) and a limit, paging through the feed as needed. Reads the community's server-rendered data, so it makes no extra API calls. Fails with a clear message when the slug does not exist or the community is private to this account, rather than returning an empty list.

### How do I automatically list community posts on skool.com?

Ask an AI agent connected to Reduck to run reduck/skool.com/list_community_posts, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/skool.com/list_community_posts

### Is there a skool.com API to list community posts?

You do not need one. "List community posts" drives the real skool.com pages in a browser, so it works whether or not skool.com offers an API for this.

### What information do I need to provide?

Required: group. Optional: limit.

### What does it return?

It returns count, group, posts, complete, totalInCommunity.

### Do I need to be logged in to skool.com?

Yes. It acts as you on skool.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the skool.com cookies saved by the Reduck extension.

### Does it change anything on skool.com, or only read data?

It only reads. It looks things up on skool.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/skool.com/list_community_posts, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/skool.com/list_community_posts

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/skool.com/list_community_posts
