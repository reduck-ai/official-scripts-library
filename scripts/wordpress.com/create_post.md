# Create a WordPress post

Automatically create a WordPress post on wordpress.com. Create a post on a WordPress site you can manage (on WordPress.com, or self-hosted where this browser is signed in to its admin), with a title and text, saved as a draft by default or published. Each line of the text becomes a paragraph. Returns the post's id, status and links, confirmed in the site's Posts screen. Publishing makes the post visible on a public site.

- Site: wordpress.com
- Address: `reduck/wordpress.com/create_post`
- Updated: 2026-11-23 (v5)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/wordpress.com/create_post`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/wordpress.com/create_post
```

## Input

- `site` (string, required): The site's address, for example mysite.wordpress.com or https://example.com.
- `title` (string, required)
- `text` (string, optional): The post's text; each line becomes a paragraph.
- `status` (any, optional): draft (default), publish, pending (for review) or private.

## Output

- `id` (integer, required)
- `site` (string, required)
- `title` (string, required)
- `status` (string, required)
- `editUrl` (string, required)
- `viewUrl` (string | null, required)
- `verified` (boolean, required): True when the Posts screen lists the post with the given title and status.

## FAQ

### What does "Create a WordPress post" do?

Create a post on a WordPress site you can manage (on WordPress.com, or self-hosted where this browser is signed in to its admin), with a title and text, saved as a draft by default or published. Each line of the text becomes a paragraph. Returns the post's id, status and links, confirmed in the site's Posts screen. Publishing makes the post visible on a public site.

### How do I automatically create a WordPress post on wordpress.com?

Ask an AI agent connected to Reduck to run reduck/wordpress.com/create_post, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/wordpress.com/create_post

### Is there a wordpress.com API to create a WordPress post?

You do not need one. "Create a WordPress post" drives the real wordpress.com pages in a browser, so it works whether or not wordpress.com offers an API for this.

### What information do I need to provide?

Required: site, title. Optional: text, status.

### What does it return?

It returns id, site, title, status, editUrl, viewUrl, verified.

### Do I need to be logged in to wordpress.com?

Yes. It acts as you on wordpress.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the wordpress.com cookies saved by the Reduck extension.

### Does it change anything on wordpress.com, or only read data?

It makes changes on wordpress.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/wordpress.com/create_post, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/wordpress.com/create_post

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/wordpress.com/create_post
