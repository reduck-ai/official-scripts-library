# List WordPress posts

Automatically list WordPress posts on wordpress.com. List the posts of a WordPress site you can manage (on WordPress.com, or self-hosted where this browser is signed in to its admin), as its Posts screen shows them, 20 per page: id, title, status (published, draft, pending, private, scheduled), slug, author id, date and links. Filter by status or search words. Pass a post's id to update_post.

- Site: wordpress.com
- Address: `reduck/wordpress.com/list_posts`
- Updated: 2026-11-04 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/wordpress.com/list_posts`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/wordpress.com/list_posts
```

## Input

- `site` (string, required): The site's address, for example mysite.wordpress.com or https://example.com.
- `page` (integer, optional)
- `search` (string, optional): Words to search for in posts, as the Posts screen's search box does.
- `status` (any, optional): Only posts with this status; any lists all but trashed posts.

## Output

- `page` (integer, required)
- `site` (string, required)
- `posts` (array, required)
- `total` (integer | null, required): How many posts match.
- `totalPages` (integer | null, required)

## FAQ

### What does "List WordPress posts" do?

List the posts of a WordPress site you can manage (on WordPress.com, or self-hosted where this browser is signed in to its admin), as its Posts screen shows them, 20 per page: id, title, status (published, draft, pending, private, scheduled), slug, author id, date and links. Filter by status or search words. Pass a post's id to update_post.

### How do I automatically list WordPress posts on wordpress.com?

Ask an AI agent connected to Reduck to run reduck/wordpress.com/list_posts, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/wordpress.com/list_posts

### Is there a wordpress.com API to list WordPress posts?

You do not need one. "List WordPress posts" drives the real wordpress.com pages in a browser, so it works whether or not wordpress.com offers an API for this.

### What information do I need to provide?

Required: site. Optional: page, search, status.

### What does it return?

It returns page, site, posts, total, totalPages.

### Do I need to be logged in to wordpress.com?

Yes. It acts as you on wordpress.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the wordpress.com cookies saved by the Reduck extension.

### Does it change anything on wordpress.com, or only read data?

It only reads. It looks things up on wordpress.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/wordpress.com/list_posts, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/wordpress.com/list_posts

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/wordpress.com/list_posts
