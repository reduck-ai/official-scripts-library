# Search X (Twitter) users by keyword, with bio and follower counts

Automatically search X (Twitter) users by keyword, with bio and follower counts on x.com. Get up to 100 accounts a run, with location, website and post count.

- Site: x.com
- Address: `reduck/x.com/search_users`
- Updated: 2026-10-06 (v1)
- Author: Reduck AI (reduck)

## About

X's People tab matches your words against names, handles and bios, which makes it good for finding people who call themselves embedded Rust developers. The catch is that the tab gives you a scrolling column of cards. Each matching account becomes one row instead, in the order X shows it rather than by follower count, with follower, following and post counts as plain numbers and the website already unwrapped from X's t.co link, so it opens the person's blog or company page. Links typed inside the bio stay as t.co, though. A developer advocate might ask for 60 accounts on "embedded rust", drop anyone under 200 posts in total, sort by followers, then check the top 25 with get_user_posts, because post count is lifetime and won't show who has gone quiet. Ask for more accounts than X will serve and you get fewer: the run gives up after two scrolls that bring nothing new.

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/x.com/search_users`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/x.com/search_users
```

## Input

- `query` (string, required): Search keyword or phrase to match against account names/handles/bios, e.g. 'AI safety researcher'. Same raw query grammar as X's People search tab.
- `count` (integer, optional): Max accounts to return. Scrolls until count is met or results dry up. Default 20, max 100.

## Output

- `count` (integer, required): Number of accounts returned. 0 is a first-class outcome (no matches).
- `query` (string, required)
- `users` (array, required)

## Example output

Shape only: placeholder values generated from the output schema, not a real run.

```json
{
  "count": 3,
  "query": "…",
  "users": [
    {
      "bio": "…",
      "name": "Example",
      "handle": "…",
      "tweets": 3,
      "user_id": "abc123",
      "website": "…",
      "location": "…",
      "verified": true,
      "followers": 1200,
      "following": 3
    }
  ]
}
```

## FAQ

### What does "Search X (Twitter) users by keyword, with bio and follower counts" do?

Search X for accounts by keyword (the People tab). Returns per account: user_id, handle, name, followers, following, tweets, verified, location, website, bio.

### How do I automatically search X (Twitter) users by keyword, with bio and follower counts on x.com?

Ask an AI agent connected to Reduck to run reduck/x.com/search_users, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/x.com/search_users

### Is there a x.com API to search X (Twitter) users by keyword, with bio and follower counts?

You do not need one. "Search X (Twitter) users by keyword, with bio and follower counts" drives the real x.com pages in a browser, so it works whether or not x.com offers an API for this.

### What information do I need to provide?

Required: query. Optional: count.

### What does it return?

It returns count, query, users.

### Do I need to be logged in to x.com?

Yes. It acts as you on x.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the x.com cookies saved by the Reduck extension.

### Does it change anything on x.com, or only read data?

It only reads. It looks things up on x.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/x.com/search_users, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/x.com/search_users

### Who maintains it?

It is part of Reduck's official curated catalogue.

### How do I get more than 100 accounts from an X user search?

One search_users run returns at most 100 X accounts (count defaults to 20), so split a big topic into narrower queries such as "embedded rust", "rust firmware" and "no_std". Merge the rows on user_id afterwards, since one account can match several of them.

### Can I filter X user search results by location or follower count?

search_users cannot filter X accounts by location or follower count, because its only inputs are query and count. Pull a bigger batch and filter on the followers and location fields afterwards, matching location loosely because it is free text the person typed, anything from "Lyon" to "somewhere in the EU".

### How much does the official X API charge to search users?

Under X's pay-per-use pricing, each user profile the official API returns costs $0.010, so a search returning 100 accounts should come to about one dollar, paid from credits bought upfront with no minimum spend. The same profile fetched again within one UTC day is billed once. The endpoint, GET /2/users/search, also needs a user-context OAuth token and pages through results with next_token.

### Does X user search show when an account joined or whether it follows me?

The rows from search_users carry no join date, no follow status and no protected flag. Run get_user_info on a handle to get joined, follows_you and is_following, and get_user_posts to see the dates of its latest posts.

Source: https://reduck.ai/explore/scripts/reduck/x.com/search_users
