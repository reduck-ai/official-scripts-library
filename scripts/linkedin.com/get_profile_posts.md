# Get LinkedIn profile posts

Automatically get LinkedIn profile posts on linkedin.com. Get a LinkedIn profile's recent posts from its activity feed by public ID, scrolling to load up to count posts. Returns each post's text, urn/url, age, engagement counts, and repost info.

- Site: linkedin.com
- Address: `reduck/linkedin.com/get_profile_posts`
- Updated: 2026-09-03 (v11)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/linkedin.com/get_profile_posts`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/linkedin.com/get_profile_posts
```

## Input

- `publicId` (string, required): LinkedIn public profile ID — the slug in linkedin.com/in/<publicId>/ (e.g. 'rob-love').
- `count` (integer, optional): Max posts to collect by scrolling the activity feed. Default 10; the feed may return fewer if exhausted.

## Output

- `posts` (array, required)

## FAQ

### What does "Get LinkedIn profile posts" do?

Get a LinkedIn profile's recent posts from its activity feed by public ID, scrolling to load up to count posts. Returns each post's text, urn/url, age, engagement counts, and repost info.

### How do I automatically get LinkedIn profile posts on linkedin.com?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/get_profile_posts, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/get_profile_posts

### Is there a linkedin.com API to get LinkedIn profile posts?

You do not need one. "Get LinkedIn profile posts" drives the real linkedin.com pages in a browser, so it works whether or not linkedin.com offers an API for this.

### What information do I need to provide?

Required: publicId. Optional: count.

### What does it return?

It returns posts.

### Do I need to be logged in to linkedin.com?

Yes. It acts as you on linkedin.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the linkedin.com cookies saved by the Reduck extension.

### Does it change anything on linkedin.com, or only read data?

It only reads. It looks things up on linkedin.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/get_profile_posts, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/get_profile_posts

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/linkedin.com/get_profile_posts
