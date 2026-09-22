# Get X post analytics

Automatically get X post analytics on x.com. Read a single X post's owner-only analytics panel (impressions, engagements, detail expands, profile visits, link clicks, and on media posts views/unique views, plus likes, reposts and replies) by post URL or id. Requires that the post belongs to the logged-in account. Returns metrics as a label-to-value list since the set varies by post type; the UI is assumed to be English, and abbreviated large counts (e.g. 1.2K) make `value` approximate. X sometimes shows a transient Retry error, so re-run on failure.

- Site: x.com
- Address: `reduck/x.com/get_post_analytics`
- Updated: 2026-09-15 (v9)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/x.com/get_post_analytics`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/x.com/get_post_analytics
```

## Input

- `post` (string, required): A post URL (e.g. https://x.com/<handle>/status/1234567890, with or without /analytics, any handle) or a bare numeric post id. The id is extracted and the handle-independent /i/status/<id>/analytics URL is used.

## Output

- `id` (string, required): The post id read from the input.
- `metrics` (array, required): One entry per metric shown in the analytics grid, in display order. The set varies by post type (media posts add Views/Unique views; posts without links omit Link clicks).
- `engagement` (object, required): The public likes/reposts/replies counts shown on the post card. Keys absent if not exposed.
- `text` (string | null, optional): The post body text as shown in the analytics card.
- `handle` (string | null, optional): @handle of the post author (the logged-in user, since analytics is owner-only).
- `postedAt` (string | null, optional): ISO timestamp the post was published (from the <time> element).

## FAQ

### What does "Get X post analytics" do?

Read a single X post's owner-only analytics panel (impressions, engagements, detail expands, profile visits, link clicks, and on media posts views/unique views, plus likes, reposts and replies) by post URL or id. Requires that the post belongs to the logged-in account. Returns metrics as a label-to-value list since the set varies by post type; the UI is assumed to be English, and abbreviated large counts (e.g. 1.2K) make `value` approximate. X sometimes shows a transient Retry error, so re-run on failure.

### How do I automatically get X post analytics on x.com?

Ask an AI agent connected to Reduck to run reduck/x.com/get_post_analytics, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/x.com/get_post_analytics

### Is there a x.com API to get X post analytics?

You do not need one. "Get X post analytics" drives the real x.com pages in a browser, so it works whether or not x.com offers an API for this.

### What information do I need to provide?

Required: post.

### What does it return?

It returns id, text, handle, metrics, postedAt, engagement.

### Do I need to be logged in to x.com?

Yes. It acts as you on x.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the x.com cookies saved by the Reduck extension.

### Does it change anything on x.com, or only read data?

It only reads. It looks things up on x.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/x.com/get_post_analytics, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/x.com/get_post_analytics

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/x.com/get_post_analytics
