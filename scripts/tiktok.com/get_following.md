# Get TikTok following

Automatically get TikTok following on tiktok.com. Lists who a TikTok account follows; other people's lists may come back capped or padded with suggestions.

- Site: tiktok.com
- Address: `reduck/tiktok.com/get_following`
- Updated: 2026-10-05 (v5)
- Author: Reduck AI (reduck)

## About

You can read who a public TikTok account follows, but for anyone other than you TikTok caps the list and fills short ones with suggested accounts, so compare total with the rows you got before trusting them. Say you pull 300 rows for a skincare brand, drop anyone above a million followers and anything flagged private, and keep the rest as a candidate list of smaller creators. If total reads 212 and 300 rows came back, at least 88 are TikTok's own suggestions, and no row says which. Each row carries the handle, nickname, bio, verified and private flags and follower count. It has no follow date, no video count and no marker for suggested accounts. Treat the result as a lead list that needs a spot check, not as a verified roster. Your own account, which you can see in full, gives the cleanest output.

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/tiktok.com/get_following`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/tiktok.com/get_following
```

## Input

- `username` (string, required): TikTok handle, with or without leading @.
- `count` (integer, optional): Target number to collect. The returned list may include TikTok's suggested accounts when the real following list is short or restricted; `total` is the declared following count.

## Output

- `total` (integer, required): Declared following count. If less than users.length, the list is padded with suggestions.
- `users` (array, required)
- `hasMore` (boolean, required)
- `username` (string, required)
- `truncated` (boolean, optional): True if TikTok flagged the list as visibility-truncated.

## Example output

Shape only: placeholder values generated from the output schema, not a real run.

```json
{
  "total": 3,
  "users": [
    {
      "id": "abc123",
      "secUid": "…",
      "nickname": "…",
      "uniqueId": "abc123",
      "verified": true,
      "signature": "…",
      "followerCount": 3.5,
      "privateAccount": true
    }
  ],
  "hasMore": true,
  "username": "…",
  "truncated": true
}
```

## FAQ

### What does "Get TikTok following" do?

List who a TikTok user follows, by @username. Accounts that keep their following list hidden, and private accounts, are reported with a clear reason instead of an empty or partial list; a handle nobody owns is reported as such. For third-party accounts, TikTok caps the list and pads short ones with suggested accounts, so check `total` and `truncated`; results are only fully reliable for accounts you can see in full, such as your own.

### How do I automatically get TikTok following on tiktok.com?

Ask an AI agent connected to Reduck to run reduck/tiktok.com/get_following, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/tiktok.com/get_following

### Is there a tiktok.com API to get TikTok following?

You do not need one. "Get TikTok following" drives the real tiktok.com pages in a browser, so it works whether or not tiktok.com offers an API for this.

### What information do I need to provide?

Required: username. Optional: count.

### What does it return?

It returns total, users, hasMore, username, truncated.

### Do I need to be logged in to tiktok.com?

No. It only uses pages of tiktok.com that are reachable without signing in.

### Does it change anything on tiktok.com, or only read data?

It only reads. It looks things up on tiktok.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/tiktok.com/get_following, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/tiktok.com/get_following

### Who maintains it?

It is part of Reduck's official curated catalogue.

### Why do some rows belong to accounts the user does not follow?

On other people's accounts TikTok may shorten the real list and top it up with suggestions. When total is lower than the number of rows, the difference is suggested accounts, and nothing in the rows tells you which ones. The truncated field is true when TikTok itself flagged the list as cut for outside viewers.

### What is the limit on how many accounts come back?

The count input goes up to 1,000, and the script requests 30 rows per page until it reaches that number or the list ends. For someone else's account TikTok usually shows less, so total is the number to trust. There is no cursor input, so if hasMore is still true after 1,000 rows, a second call cannot continue from there. An empty reply from TikTok ends the run with a rate limit error, which points at the signed-in browser's account or IP, not the one you looked up.

### What happens with a private account or a hidden following list?

The run fails with an error that says which case it is, a private account or a following list kept private, instead of returning nothing. A typo in the handle fails with an error saying the account does not exist. A hidden list can still be worked around from the other side, since followers of that account are often visible through the get_followers script.

Source: https://reduck.ai/explore/scripts/reduck/tiktok.com/get_following
