# Get LinkedIn group posts

Automatically get LinkedIn group posts on linkedin.com. Fetch posts from a LinkedIn group feed by group id, newest-first, with author, text, age and reaction count. Public groups are readable without joining; a private group you are not a member of returns an empty list flagged restricted rather than failing.

- Site: linkedin.com
- Address: `reduck/linkedin.com/get_group_posts`
- Updated: 2026-09-03 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/linkedin.com/get_group_posts`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/linkedin.com/get_group_posts
```

## Input

- `groupId` (string, required): LinkedIn group id, the number in the group URL e.g. "8794032" for linkedin.com/groups/8794032/. A full group URL is also accepted and the id is extracted from it.
- `limit` (integer, optional): Maximum posts to return, newest-first. The feed loads 5 more per scroll; fewer are returned if the feed runs out.

## Output

- `posts` (array, required)
- `group_id` (string, required)
- `group_name` (string | null, required): Group display name from the page header.
- `note` (string | null, optional)
- `restricted` (boolean, optional): True when the group exists but no posts are visible — a private group this account has not joined. posts is then empty. A nonexistent id throws instead.

## FAQ

### What does "Get LinkedIn group posts" do?

Fetch posts from a LinkedIn group feed by group id, newest-first, with author, text, age and reaction count. Public groups are readable without joining; a private group you are not a member of returns an empty list flagged restricted rather than failing.

### How do I automatically get LinkedIn group posts on linkedin.com?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/get_group_posts, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/get_group_posts

### Is there a linkedin.com API to get LinkedIn group posts?

You do not need one. "Get LinkedIn group posts" drives the real linkedin.com pages in a browser, so it works whether or not linkedin.com offers an API for this.

### What information do I need to provide?

Required: groupId. Optional: limit.

### What does it return?

It returns note, posts, group_id, group_name, restricted.

### Do I need to be logged in to linkedin.com?

Yes. It acts as you on linkedin.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the linkedin.com cookies saved by the Reduck extension.

### Does it change anything on linkedin.com, or only read data?

It only reads. It looks things up on linkedin.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/get_group_posts, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/get_group_posts

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/linkedin.com/get_group_posts
