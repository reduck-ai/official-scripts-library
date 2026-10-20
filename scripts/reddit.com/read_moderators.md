# Read Reddit subreddit moderators

Automatically read Reddit subreddit moderators on reddit.com. An unofficial Reddit API: read the full moderator list of a subreddit programmatically, from code or from an AI agent, with typed JSON in and out. Reddit's API needs a registered app and OAuth, and its mod-list endpoint is closed to logged-out callers.

- Site: reddit.com
- Address: `reduck/reddit.com/read_moderators`
- Updated: 2026-10-19 (v6)
- Author: Reduck AI (reduck)

## About

Developers looking for a Reddit API to read the full moderator list of a subreddit usually find there is none they can use: Reddit's API needs a registered app and OAuth, and its mod-list endpoint is closed to logged-out callers. This script fills that gap. It works like an API endpoint — one call with typed arguments, a JSON response — but runs through a real browser, yours or a hosted one, so it needs no Reddit developer account, API key or app review.

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/reddit.com/read_moderators`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/reddit.com/read_moderators
```

## Input

- `subreddit` (string, optional): Subreddit name, with or without the r/ prefix, e.g. "LocalLLaMA".
- `subreddits` (array, optional): Not supported since 19 Oct 2026: the run fails with a message saying so. Send one subreddit per call and fan out with run_script's scripts.

## Output

- `subreddit` (string, required)
- `moderators` (array, required): Every moderator of the subreddit, in Reddit's order.

## Example output

Shape only: placeholder values generated from the output schema, not a real run.

```json
{
  "subreddit": "…",
  "moderators": [
    {
      "name": "Example",
      "perms": [
        "…"
      ]
    }
  ]
}
```

## FAQ

### What does "Read Reddit subreddit moderators" do?

Returns the complete moderator list of one subreddit, every moderator rather than just the first screen the mod page shows, with each one's permissions, in Reddit's order. Requires being signed in to Reddit. A banned or private subreddit fails with Reddit's reason. To read several subreddits, run the script once per subreddit (fan out with run_script's scripts). Until 19 Oct 2026 the argument was a `subreddits` list answering {perSubreddit, overlaps, counts}; a call still sending it fails with a message saying so, and overlaps and counts are the caller's to derive.

### How do I automatically read Reddit subreddit moderators on reddit.com?

Ask an AI agent connected to Reduck to run reduck/reddit.com/read_moderators, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/reddit.com/read_moderators

### Is there a reddit.com API to read Reddit subreddit moderators?

You do not need one. "Read Reddit subreddit moderators" drives the real reddit.com pages in a browser, so it works whether or not reddit.com offers an API for this.

### What information do I need to provide?

Optional: subreddit, subreddits.

### What does it return?

It returns subreddit, moderators.

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
