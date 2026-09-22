# Get Product Hunt launch comments

Automatically get Product Hunt launch comments on producthunt.com. Read the comment thread on a Product Hunt launch. Returns each comment with its author (name, handle, profile id and the product they are credited to), the text, its upvote count, when it was posted, whether it is pinned, and how deeply it is nested so replies stay attached to what they answer. Accepts a full launch URL or a "product/launch" slug pair. Product Hunt's headline comment tally on a launch counts more items than the thread actually renders, so both numbers are returned side by side rather than presenting the visible ones as the complete set. An unknown launch is reported as such.

- Site: producthunt.com
- Address: `reduck/producthunt.com/get_launch_comments`
- Updated: 2026-08-28 (v5)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/producthunt.com/get_launch_comments`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/producthunt.com/get_launch_comments
```

## Input

- `launch` (string, required): Full launch URL (e.g. "https://www.producthunt.com/products/notion/launches/notion-mail") or a "product/launch" slug pair (e.g. "notion/notion-mail").

## Output

- `comments` (array, required)
- `returned` (number, required): How many comments this read actually returned.
- `launchUrl` (string, required)
- `launchSlug` (string, required)
- `productSlug` (string, required)
- `reportedTotal` (number | null, required): The comment tally Product Hunt prints for the launch. It counts more than the thread renders, so it is normally HIGHER than `returned` — that difference is expected, not a failed read. Null when the page prints no tally.
- `sortApplied` (string | null, optional): Which ordering the thread was showing, as labelled on the page. Product Hunt defaults to its own "best" ordering; this script does not change it. Null when the launch has no thread yet.

## FAQ

### What does "Get Product Hunt launch comments" do?

Read the comment thread on a Product Hunt launch. Returns each comment with its author (name, handle, profile id and the product they are credited to), the text, its upvote count, when it was posted, whether it is pinned, and how deeply it is nested so replies stay attached to what they answer. Accepts a full launch URL or a "product/launch" slug pair. Product Hunt's headline comment tally on a launch counts more items than the thread actually renders, so both numbers are returned side by side rather than presenting the visible ones as the complete set. An unknown launch is reported as such.

### How do I automatically get Product Hunt launch comments on producthunt.com?

Ask an AI agent connected to Reduck to run reduck/producthunt.com/get_launch_comments, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/producthunt.com/get_launch_comments

### Is there a producthunt.com API to get Product Hunt launch comments?

You do not need one. "Get Product Hunt launch comments" drives the real producthunt.com pages in a browser, so it works whether or not producthunt.com offers an API for this.

### What information do I need to provide?

Required: launch.

### What does it return?

It returns comments, returned, launchUrl, launchSlug, productSlug, sortApplied, reportedTotal.

### Do I need to be logged in to producthunt.com?

Yes. It acts as you on producthunt.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the producthunt.com cookies saved by the Reduck extension.

### Does it change anything on producthunt.com, or only read data?

It only reads. It looks things up on producthunt.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/producthunt.com/get_launch_comments, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/producthunt.com/get_launch_comments

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/producthunt.com/get_launch_comments
