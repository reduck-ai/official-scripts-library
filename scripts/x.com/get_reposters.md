# Get post reposters

Automatically get post reposters on x.com. List the accounts that reposted (retweeted) an X post, by post URL. Returns per account: user_id, handle, name, followers, following, tweets, verified, location, website, bio. X returns a sample of reposters, not the full set: high-repost posts cap out a few hundred deep.

- Site: x.com
- Address: `reduck/x.com/get_reposters`
- Updated: 2026-09-03 (v4)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/x.com/get_reposters`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/x.com/get_reposters
```

## Input

- `url` (string, required): Full URL of the X post, e.g. 'https://x.com/<handle>/status/<id>'. Query/hash are stripped.
- `count` (integer, optional): Max reposters to return. Scrolls until count is met or the list dries up. Default 100.

## Output

- `url` (string, required)
- `count` (integer, required): Number of reposters returned. 0 is a first-class outcome (no reposts, or reposters hidden).
- `reposters` (array, required)
- `account_used` (string | null, required): handle of the logged-in account that performed this lookup, read from the account switcher UI (not assumed from input) — audit-trail consistency with the action scripts.

## FAQ

### What does "Get post reposters" do?

List the accounts that reposted (retweeted) an X post, by post URL. Returns per account: user_id, handle, name, followers, following, tweets, verified, location, website, bio. X returns a sample of reposters, not the full set: high-repost posts cap out a few hundred deep.

### How do I automatically get post reposters on x.com?

Ask an AI agent connected to Reduck to run reduck/x.com/get_reposters, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/x.com/get_reposters

### Is there a x.com API to get post reposters?

You do not need one. "Get post reposters" drives the real x.com pages in a browser, so it works whether or not x.com offers an API for this.

### What information do I need to provide?

Required: url. Optional: count.

### What does it return?

It returns url, count, reposters, account_used.

### Do I need to be logged in to x.com?

Yes. It acts as you on x.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the x.com cookies saved by the Reduck extension.

### Does it change anything on x.com, or only read data?

It only reads. It looks things up on x.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/x.com/get_reposters, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/x.com/get_reposters

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/x.com/get_reposters
