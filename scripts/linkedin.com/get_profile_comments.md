# Get LinkedIn profile comments

Automatically get LinkedIn profile comments on linkedin.com. Get the comments a LinkedIn profile has left on posts, from its Comments activity feed by public ID, scrolling to load up to count comments. Returns each comment's text/urn/age/reactions and the post it was made on (author, text, url).

- Site: linkedin.com
- Address: `reduck/linkedin.com/get_profile_comments`
- Updated: 2026-09-03 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/linkedin.com/get_profile_comments`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/linkedin.com/get_profile_comments
```

## Input

- `publicId` (string, required): LinkedIn public profile ID — the slug in linkedin.com/in/<publicId>/ (e.g. 'peter-csiba').
- `count` (integer, optional): Max number of the owner's comments to collect by scrolling the Comments activity feed. Default 10; the feed may return fewer if exhausted.

## Output

- `comments` (array, required)

## FAQ

### What does "Get LinkedIn profile comments" do?

Get the comments a LinkedIn profile has left on posts, from its Comments activity feed by public ID, scrolling to load up to count comments. Returns each comment's text/urn/age/reactions and the post it was made on (author, text, url).

### How do I automatically get LinkedIn profile comments on linkedin.com?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/get_profile_comments, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/get_profile_comments

### Is there a linkedin.com API to get LinkedIn profile comments?

You do not need one. "Get LinkedIn profile comments" drives the real linkedin.com pages in a browser, so it works whether or not linkedin.com offers an API for this.

### What information do I need to provide?

Required: publicId. Optional: count.

### What does it return?

It returns comments.

### Do I need to be logged in to linkedin.com?

Yes. It acts as you on linkedin.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the linkedin.com cookies saved by the Reduck extension.

### Does it change anything on linkedin.com, or only read data?

Unknown: its author has not declared whether it changes anything on linkedin.com, so treat it as if it could.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/get_profile_comments, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/get_profile_comments

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/linkedin.com/get_profile_comments
