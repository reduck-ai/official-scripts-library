# See who reposted (retweeted) a post on X (Twitter)

Each reposter comes back as one row with followers, following, bio and website.

- Site: x.com
- Address: `reduck/x.com/get_reposters`
- Updated: 2026-10-05 (v4)
- Author: Reduck AI (reduck)

## About

X already lists who reposted a public post on its Reposts tab (the post URL plus /retweets), but only as a feed you scroll by hand. get_reposters opens that tab, keeps scrolling, and turns each account into a row you can sort. The count input defaults to 100 and goes up to 1,000, so raise it for a busy post. A founder whose launch post picked up 180 reposts runs it with count at 200, sorts by followers, and finds four accounts with large followings next to a cluster of blank-bio accounts each following about 5,000 people, which looks a lot like an engagement pod. Those four go into a private X List (create_list, then add_to_list per handle) so the founder can watch what they post next. The catch is that X serves a sample of reposters rather than the full set, so on a viral post the list stops a few hundred in whatever count you ask for.

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

## Example output

Shape only: placeholder values generated from the output schema, not a real run.

```json
{
  "url": "https://example.com/item/123",
  "count": 3,
  "reposters": [
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
  ],
  "account_used": "…"
}
```

## FAQ

### What does "See who reposted (retweeted) a post on X (Twitter)" do?

List the accounts that reposted (retweeted) an X post, by post URL. Returns per account: user_id, handle, name, followers, following, tweets, verified, location, website, bio. X returns a sample of reposters, not the full set: high-repost posts cap out a few hundred deep.

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

### Why did I get fewer reposters than the repost count on the post?

The count input defaults to 100, so a post with 250 reposts returns 100 rows unless you raise it (1,000 is the max). Past that, X serves only a sample of reposters and the list dries up a few hundred deep however high you set count. Asking for more than X will serve costs nothing but a short wait, because the run ends once three scrolls in a row bring no new accounts.

### Can it also show who liked or quoted the post?

get_reposters covers reposts only. Quotes have their own script, get_quote_tweets, which returns each quoting tweet with its text and post time. Likes have been private on X since June 2024, visible only to the post's author, and Reduck has no script that exports likers.

### What would the official X API charge for the same list?

On X's pay-per-use plan each user returned is billed as a user read at $0.010, so a full page of 100 reposters costs about $1 in credits bought upfront, and a user already billed that UTC day is not charged again. X's integration guide also says the retweeted_by endpoint returns only the 100 most recent reposting users, at 75 requests per 15 minutes, so paying more does not get you further down the list.

### Does it show when each account reposted, or who reposted first?

get_reposters returns no repost time. Each row is a profile only and the order is whatever X serves, so the output cannot rank reposters by time or tell you whether the reposts came in one burst. Quote tweets are different: get_quote_tweets returns a created_at for each quoting tweet.

Source: https://reduck.ai/explore/scripts/reduck/x.com/get_reposters
