# Reddit API: read the full moderator list of subreddits

Automatically read the full moderator list of subreddits on reddit.com. An unofficial Reddit API: read the full moderator list of a subreddit programmatically, from code or from an AI agent, with typed JSON in and out. Reddit's API needs a registered app and OAuth, and its mod-list endpoint is closed to logged-out callers.

- Site: reddit.com
- Address: `reduck/reddit.com/read_moderators`
- Updated: 2026-09-18 (v1)
- Author: Reduck AI (reduck)

## About

Developers looking for a Reddit API to read the full moderator list of a subreddit usually find there is none they can use: Reddit's API needs a registered app and OAuth, and its mod-list endpoint is closed to logged-out callers. This script fills that gap. It works like an API endpoint — one call with typed arguments, a JSON response — but runs through a real browser, yours or a hosted one, so it needs no Reddit developer account, API key or app review.

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/reddit.com/read_moderators`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/reddit.com/read_moderators
```

## Input

- `subreddits` (array, required): Subreddit names without the r/ prefix, e.g. ["AI_Agents","LocalLLaMA"]

## Output

- `counts` (object, optional)
- `overlaps` (array, optional)
- `perSubreddit` (object, optional)

## Example output

Shape only: placeholder values generated from the output schema, not a real run.

```json
{
  "counts": {},
  "overlaps": [],
  "perSubreddit": {}
}
```

## FAQ

### What does "Reddit API: read the full moderator list of subreddits" do?

Returns the complete moderator list of each subreddit you ask for — every moderator, not just the first screen the mod page shows — with each one's permissions. Also reports, per moderator, which of the requested subreddits they moderate, so you can see who sits on several communities at once and how much their mod teams overlap.

### How do I automatically read the full moderator list of subreddits on reddit.com?

Ask an AI agent connected to Reduck to run reduck/reddit.com/read_moderators, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/reddit.com/read_moderators

### Is there a reddit.com API to read the full moderator list of subreddits?

You do not need one. "Reddit API: read the full moderator list of subreddits" drives the real reddit.com pages in a browser, so it works whether or not reddit.com offers an API for this.

### What information do I need to provide?

Required: subreddits.

### What does it return?

It returns counts, overlaps, perSubreddit.

### Do I need to be logged in to reddit.com?

Yes. It acts as you on reddit.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the reddit.com cookies saved by the Reduck extension.

### Does it change anything on reddit.com, or only read data?

It only reads. It looks things up on reddit.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/reddit.com/read_moderators, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/reddit.com/read_moderators

### Who maintains it?

It is part of Reduck's official curated catalogue.

### Is there a Reddit API to read the full moderator list of a subreddit?

Not an official one you can use for this: Reddit's API needs a registered app and OAuth, and its mod-list endpoint is closed to logged-out callers. This script works as an unofficial Reddit API for it: typed input, JSON output, callable from an AI agent over MCP, from the CLI, or over REST.

### How do I read the full moderator list of a subreddit programmatically?

Call this script with its arguments and read the JSON it returns. It drives Reddit in a real browser session, so there is no API key to request and nothing to reverse-engineer yourself.

Source: https://reduck.ai/explore/scripts/reduck/reddit.com/read_moderators
