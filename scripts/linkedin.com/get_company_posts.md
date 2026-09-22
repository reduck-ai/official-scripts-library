# Get LinkedIn company posts

Automatically get LinkedIn company posts on linkedin.com. Get the most recent posts of a LinkedIn company page (newest first) from its URL or slug, up to count. Returns company, total, and posts (activityId, url, text, postedAt, age, isRepost, reactions, comments, reposts).

- Site: linkedin.com
- Address: `reduck/linkedin.com/get_company_posts`
- Updated: 2026-09-03 (v11)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/linkedin.com/get_company_posts`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/linkedin.com/get_company_posts
```

## Input

- `company` (string, required): LinkedIn company page URL (e.g. https://www.linkedin.com/company/fintech-collective/) or bare slug (fintech-collective).
- `count` (integer, optional): How many of the most recent posts to return. Default 10 (one feed fetch); above 10 the script scroll-paginates by 10 per round. Capped at 50.

## Output

- `posts` (array, required): Newest first (ordered by activity id, which encodes the timestamp — NOT by the feed's display order).
- `total` (integer, required): Total posts on the page, from the feed module's paging metadata in the cold SSR blob. 0 with posts:[] = page has never posted ('No posts yet' state, first-class outcome).
- `company` (string, required): Slug as requested (after URL parsing).

## FAQ

### What does "Get LinkedIn company posts" do?

Get the most recent posts of a LinkedIn company page (newest first) from its URL or slug, up to count. Returns company, total, and posts (activityId, url, text, postedAt, age, isRepost, reactions, comments, reposts).

### How do I automatically get LinkedIn company posts on linkedin.com?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/get_company_posts, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/get_company_posts

### Is there a linkedin.com API to get LinkedIn company posts?

You do not need one. "Get LinkedIn company posts" drives the real linkedin.com pages in a browser, so it works whether or not linkedin.com offers an API for this.

### What information do I need to provide?

Required: company. Optional: count.

### What does it return?

It returns posts, total, company.

### Do I need to be logged in to linkedin.com?

Yes. It acts as you on linkedin.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the linkedin.com cookies saved by the Reduck extension.

### Does it change anything on linkedin.com, or only read data?

It only reads. It looks things up on linkedin.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/get_company_posts, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/get_company_posts

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/linkedin.com/get_company_posts
