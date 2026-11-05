# Update a WordPress post

Automatically update a WordPress post on wordpress.com. Change a post on a WordPress site you can manage: its title, its text (replaced whole; each line becomes a paragraph) and/or its status (draft, publish, pending, private). Fields you leave out keep their values. Returns the post as the site's Posts screen then lists it. Get post ids from list_posts. Publishing makes the post visible on a public site.

- Site: wordpress.com
- Address: `reduck/wordpress.com/update_post`
- Updated: 2026-11-04 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/wordpress.com/update_post`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/wordpress.com/update_post
```

## Input

- `id` (integer, required): The post's id, from list_posts or create_post.
- `site` (string, required): The site's address, for example mysite.wordpress.com or https://example.com.
- `text` (string, optional): New text for the whole post; each line becomes a paragraph.
- `title` (string, optional)
- `status` (any, optional)

## Output

- `id` (integer, required)
- `site` (string, required)
- `title` (string, required)
- `status` (string, required)
- `changed` (array, required): Which of title, text and status were changed.
- `verified` (boolean, required): True when the Posts screen lists the post with the new title and status.
- `viewUrl` (string | null, optional)

## FAQ

### What does "Update a WordPress post" do?

Change a post on a WordPress site you can manage: its title, its text (replaced whole; each line becomes a paragraph) and/or its status (draft, publish, pending, private). Fields you leave out keep their values. Returns the post as the site's Posts screen then lists it. Get post ids from list_posts. Publishing makes the post visible on a public site.

### How do I automatically update a WordPress post on wordpress.com?

Ask an AI agent connected to Reduck to run reduck/wordpress.com/update_post, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/wordpress.com/update_post

### Is there a wordpress.com API to update a WordPress post?

You do not need one. "Update a WordPress post" drives the real wordpress.com pages in a browser, so it works whether or not wordpress.com offers an API for this.

### What information do I need to provide?

Required: site, id. Optional: text, title, status.

### What does it return?

It returns id, site, title, status, changed, viewUrl, verified.

### Do I need to be logged in to wordpress.com?

Yes. It acts as you on wordpress.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the wordpress.com cookies saved by the Reduck extension.

### Does it change anything on wordpress.com, or only read data?

It makes changes on wordpress.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/wordpress.com/update_post, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/wordpress.com/update_post

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/wordpress.com/update_post
