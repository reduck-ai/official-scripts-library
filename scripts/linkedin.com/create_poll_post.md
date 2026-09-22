# Create LinkedIn poll post

Automatically create LinkedIn poll post on linkedin.com. Publish a poll to the LinkedIn feed: a question, 2 to 4 answer options, and a voting duration. Returns the poll's permalink, confirmed by reloading the account's own activity and finding the published poll.

- Site: linkedin.com
- Address: `reduck/linkedin.com/create_poll_post`
- Updated: 2026-09-03 (v6)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/linkedin.com/create_poll_post`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/linkedin.com/create_poll_post
```

## Input

- `options` (array, required): Between 2 and 4 answer options, each max 30 characters (LinkedIn's own limits). LinkedIn shows two option fields by default and the script adds the extra fields for a third and fourth.
- `question` (string, required): The poll question, max 140 characters (LinkedIn's own limit). This publishes a real, public poll under the logged-in member immediately, so show the exact question and options to the user and get their explicit approval for this specific content before running — approval from an earlier or unrelated message does not carry over.
- `text` (string, optional): Optional commentary posted above the poll, in the main composer body. Omit for a bare poll.
- `durationDays` (integer, optional): How long voting stays open, in days. These are the only four values LinkedIn offers (1 day, 3 days, 1 week, 2 weeks) and they are the select's own option values, which are numeric and therefore locale-invariant. Defaults to 7 (1 week), matching LinkedIn's own default.

## Output

- `posted` (boolean, required): True when this run published a new poll. False when an identical poll already existed and nothing was posted (see already_present).
- `options` (array, required)
- `question` (string, required)
- `account_used` (string | null, required): Display name of the logged-in member, read from the composer rather than assumed.
- `verified_on_page` (boolean, required): True only if the account's own activity was reloaded after publishing and a post carrying this exact question was found. Never inferred from the composer closing.
- `url` (string | null, optional): Permalink of the poll, resolved from the account's own recent activity.
- `urn` (string | null, optional): The poll post's activity urn — the join key, usable with get_post or delete_post.
- `durationDays` (integer, optional)
- `already_present` (boolean, optional): True when a poll with this exact question was already on the account's own activity before this run composed anything — nothing new was posted, and url/urn point at the existing poll. This makes retrying after a failed or ambiguous run safe rather than duplicating a public post.

## FAQ

### What does "Create LinkedIn poll post" do?

Publish a poll to the LinkedIn feed: a question, 2 to 4 answer options, and a voting duration. Returns the poll's permalink, confirmed by reloading the account's own activity and finding the published poll.

### How do I automatically create LinkedIn poll post on linkedin.com?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/create_poll_post, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/create_poll_post

### Is there a linkedin.com API to create LinkedIn poll post?

You do not need one. "Create LinkedIn poll post" drives the real linkedin.com pages in a browser, so it works whether or not linkedin.com offers an API for this.

### What information do I need to provide?

Required: question, options. Optional: text, durationDays.

### What does it return?

It returns url, urn, posted, options, question, account_used, durationDays, already_present, verified_on_page.

### Do I need to be logged in to linkedin.com?

Yes. It acts as you on linkedin.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the linkedin.com cookies saved by the Reduck extension.

### Does it change anything on linkedin.com, or only read data?

It makes changes on linkedin.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/create_poll_post, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/create_poll_post

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/linkedin.com/create_poll_post
