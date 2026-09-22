# Get LinkedIn saved posts

Automatically get LinkedIn saved posts on linkedin.com. Get the logged-in member's saved LinkedIn posts (My Items > Saved posts), scrolling/loading more to collect up to count. Returns each post's author, headline, degree, text, age, and permalink. Empty list when nothing is saved.

- Site: linkedin.com
- Address: `reduck/linkedin.com/get_saved_posts`
- Updated: 2026-09-03 (v5)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/linkedin.com/get_saved_posts`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/linkedin.com/get_saved_posts
```

## Input

- `count` (integer, optional): Max saved posts to collect, clicking 'Show more results' as needed.

## Output

- `posts` (array, required)

## FAQ

### What does "Get LinkedIn saved posts" do?

Get the logged-in member's saved LinkedIn posts (My Items > Saved posts), scrolling/loading more to collect up to count. Returns each post's author, headline, degree, text, age, and permalink. Empty list when nothing is saved.

### How do I automatically get LinkedIn saved posts on linkedin.com?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/get_saved_posts, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/get_saved_posts

### Is there a linkedin.com API to get LinkedIn saved posts?

You do not need one. "Get LinkedIn saved posts" drives the real linkedin.com pages in a browser, so it works whether or not linkedin.com offers an API for this.

### What information do I need to provide?

Optional: count.

### What does it return?

It returns posts.

### Do I need to be logged in to linkedin.com?

Yes. It acts as you on linkedin.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the linkedin.com cookies saved by the Reduck extension.

### Does it change anything on linkedin.com, or only read data?

It only reads. It looks things up on linkedin.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/get_saved_posts, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/get_saved_posts

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/linkedin.com/get_saved_posts
