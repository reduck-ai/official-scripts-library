# List Instagram posts tagged at a location

Automatically list Instagram posts tagged at a location on instagram.com. Search Instagram for a place by name and list posts tagged there (the location page's "Top" grid). Returns the matched location's name, id and city, plus each post's code, owner username, caption and thumbnail image URL.

- Site: instagram.com
- Address: `reduck/instagram.com/get_location_posts`
- Updated: 2026-09-18 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/instagram.com/get_location_posts`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/instagram.com/get_location_posts
```

## Input

- `query` (string, required): Place name to search for, e.g. "Louvre Museum", "Eiffel Tower"

## Output

- `count` (integer, required)
- `posts` (array, required)
- `location` (object, required)

## FAQ

### What does "List Instagram posts tagged at a location" do?

Search Instagram for a place by name and list posts tagged there (the location page's "Top" grid). Returns the matched location's name, id and city, plus each post's code, owner username, caption and thumbnail image URL.

### How do I automatically list Instagram posts tagged at a location on instagram.com?

Ask an AI agent connected to Reduck to run reduck/instagram.com/get_location_posts, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/instagram.com/get_location_posts

### Is there a instagram.com API to list Instagram posts tagged at a location?

You do not need one. "List Instagram posts tagged at a location" drives the real instagram.com pages in a browser, so it works whether or not instagram.com offers an API for this.

### What information do I need to provide?

Required: query.

### What does it return?

It returns count, posts, location.

### Do I need to be logged in to instagram.com?

Yes. It acts as you on instagram.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the instagram.com cookies saved by the Reduck extension.

### Does it change anything on instagram.com, or only read data?

It only reads. It looks things up on instagram.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/instagram.com/get_location_posts, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/instagram.com/get_location_posts

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/instagram.com/get_location_posts
