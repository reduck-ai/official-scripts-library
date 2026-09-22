# Get LinkedIn post

Automatically get LinkedIn post on linkedin.com. Fetch a single LinkedIn post by its permalink. Returns url, urn, text, media, author (name, headline, url, type), postedAgo, reactions, comments, and reposts. If the URL has no post behind it — deleted, removed, or a wrong id — it says so straight away instead of stalling. Use get_post_comments for the thread and get_post_reactors for who reacted.

- Site: linkedin.com
- Address: `reduck/linkedin.com/get_post`
- Updated: 2026-09-03 (v34)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/linkedin.com/get_post`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/linkedin.com/get_post
```

## Input

- `postUrl` (string, required): LinkedIn post permalink, e.g. https://www.linkedin.com/posts/<slug>-<id>-<code>/ or https://www.linkedin.com/feed/update/urn:li:activity:<id>/. Query string is stripped. A sponsored post's permalink has no viewable page and will be refused.

## Output

- `url` (string, required)
- `urn` (string | null, optional): Displayed identity: signed in, from the reaction facepile (urn:li:activity:… or urn:li:ugcPost:…, may differ from the URL's id); signed out, the guest card's own data-activity-urn. Null only if that element doesn't render (rare) — not tied to a zero reaction count.
- `text` (string | null, optional): Commentary text; null on media-only posts — and on a quote-reshare with no commentary of its own (the quoted content is in quotedPost, never here). Signed out this is the LD articleBody, the full untruncated commentary.
- `media` (string, optional): video | image | document | none (best-effort; a multi-image carousel reads as image)
- `author` (object, optional)
- `reposts` (number | null, optional): Null signed-out: the guest action bar renders no repost control and the LD carries no repost statistic, so the count is unobserved rather than zero.
- `comments` (number | null, optional)
- `postedAgo` (string | null, optional)
- `reactions` (number | null, optional)
- `quotedPost` (object | null, optional): The embedded original when this post is a quote-reshare ('repost with thoughts'). Null when the post embeds no quoted update. On the SDUI shell the quoted author's headline is not extracted (null).
- `datePublished` (string | null, optional): ISO instant the post was published, from the signed-out page's schema.org block. Null on the signed-in shells, which render only a relative age — so when an exact time matters, a managed (signed-out) run is the one that has it.

## FAQ

### What does "Get LinkedIn post" do?

Fetch a single LinkedIn post by its permalink. Returns url, urn, text, media, author (name, headline, url, type), postedAgo, reactions, comments, and reposts. If the URL has no post behind it — deleted, removed, or a wrong id — it says so straight away instead of stalling. Use get_post_comments for the thread and get_post_reactors for who reacted.

### How do I automatically get LinkedIn post on linkedin.com?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/get_post, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/get_post

### Is there a linkedin.com API to get LinkedIn post?

You do not need one. "Get LinkedIn post" drives the real linkedin.com pages in a browser, so it works whether or not linkedin.com offers an API for this.

### What information do I need to provide?

Required: postUrl.

### What does it return?

It returns url, urn, text, media, author, reposts, comments, postedAgo, reactions, quotedPost, datePublished.

### Do I need to be logged in to linkedin.com?

No. It only uses pages of linkedin.com that are reachable without signing in.

### Does it change anything on linkedin.com, or only read data?

It only reads. It looks things up on linkedin.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/get_post, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/get_post

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/linkedin.com/get_post
