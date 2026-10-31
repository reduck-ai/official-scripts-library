# List Skool community posts

Automatically list Skool community posts on skool.com. List one page of the posts in a Skool community feed, in the order Skool shows them, pinned posts first on page 1. Returns per post the title, body text, author name and handle, creation time, comment and upvote counts, whether it is pinned, the channel it was posted in, and a direct url, plus the community's total post count. Takes the community slug as it appears in the URL (case-insensitive) and a page number; ask for the next page until one returns no posts. Fails with a clear message when the slug does not exist, the community is private to this account, or the browser is not signed in to Skool.

- Site: skool.com
- Address: `reduck/skool.com/list_community_posts`
- Updated: 2026-10-30 (v9)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/skool.com/list_community_posts`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/skool.com/list_community_posts
```

## Input

- `group` (string, required): Community slug as it appears in the URL, e.g. "cliefnotes" for https://www.skool.com/cliefnotes. Case-insensitive.
- `page` (integer, optional): Feed page, as Skool pages it (about 30 posts each). Ask for the next page until a page returns no posts.

## Output

- `page` (integer, required)
- `count` (integer, required)
- `group` (string, required)
- `posts` (array, required)
- `totalInCommunity` (integer | null, required): Total posts Skool reports for this community.

## FAQ

### What does "List Skool community posts" do?

List one page of the posts in a Skool community feed, in the order Skool shows them, pinned posts first on page 1. Returns per post the title, body text, author name and handle, creation time, comment and upvote counts, whether it is pinned, the channel it was posted in, and a direct url, plus the community's total post count. Takes the community slug as it appears in the URL (case-insensitive) and a page number; ask for the next page until one returns no posts. Fails with a clear message when the slug does not exist, the community is private to this account, or the browser is not signed in to Skool.

### How do I automatically list Skool community posts on skool.com?

Ask an AI agent connected to Reduck to run reduck/skool.com/list_community_posts, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/skool.com/list_community_posts

### Is there a skool.com API to list Skool community posts?

You do not need one. "List Skool community posts" drives the real skool.com pages in a browser, so it works whether or not skool.com offers an API for this.

### What information do I need to provide?

Required: group. Optional: page.

### What does it return?

It returns page, count, group, posts, totalInCommunity.

### Do I need to be logged in to skool.com?

Yes. It acts as you on skool.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the skool.com cookies saved by the Reduck extension.

### Does it change anything on skool.com, or only read data?

It only reads. It looks things up on skool.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/skool.com/list_community_posts, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/skool.com/list_community_posts

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/skool.com/list_community_posts
