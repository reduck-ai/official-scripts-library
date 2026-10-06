# Search TikTok users

Automatically search TikTok users on tiktok.com. Type part of a name or @handle and get the 10 or so accounts TikTok matches, with followers, likes and bio.

- Site: tiktok.com
- Address: `reduck/tiktok.com/search_users`
- Updated: 2026-10-05 (v2)
- Author: Reduck AI (reduck)

## About

TikTok's user search is where you go when you half remember a creator's name, or want to see who else is trading on your brand. You get the first batch TikTok matches, usually about 10 accounts, each with its @handle, bio, follower count, total likes and verified flag, which is normally enough to tell the real account from a fan page. A small Lyon candle shop's social lead, for example, searches the shop's name every Monday, sets its own account aside, sorts the rest by followerCount and runs get_profile on the top few to see which are private or only a few weeks old. The catch is volume. There is no next-page option, so wider coverage means more spellings, or a city or niche word added to the name. Searches need a browser signed in to TikTok. If TikTok sends back a blank response, the run reloads and retries, three attempts in all, then stops with an error.

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/tiktok.com/search_users`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/tiktok.com/search_users
```

## Input

- `query` (string, required): Search keyword(s) — name or handle fragment.

## Output

- `query` (string, required)
- `total` (integer, required): Number of users returned (TikTok web caps this around 10 per query; the endpoint's has_more/count/offset are non-functional for this surface, so there is no deeper page).
- `users` (array, required)

## Example output

Shape only: placeholder values generated from the output schema, not a real run.

```json
{
  "query": "…",
  "total": 3,
  "users": [
    {
      "id": "abc123",
      "secUid": "…",
      "nickname": "…",
      "uniqueId": "abc123",
      "verified": true,
      "signature": "…",
      "heartCount": 3.5,
      "followerCount": 3.5
    }
  ]
}
```

## FAQ

### What does "Search TikTok users" do?

Search TikTok accounts by keyword. Returns the top ~10 matches (TikTok web caps user search; not deeply paginable).

### How do I automatically search TikTok users on tiktok.com?

Ask an AI agent connected to Reduck to run reduck/tiktok.com/search_users, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/tiktok.com/search_users

### Is there a tiktok.com API to search TikTok users?

You do not need one. "Search TikTok users" drives the real tiktok.com pages in a browser, so it works whether or not tiktok.com offers an API for this.

### What information do I need to provide?

Required: query.

### What does it return?

It returns query, total, users.

### Do I need to be logged in to tiktok.com?

Yes. It acts as you on tiktok.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the tiktok.com cookies saved by the Reduck extension.

### Does it change anything on tiktok.com, or only read data?

Unknown: its author has not declared whether it changes anything on tiktok.com, so treat it as if it could.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/tiktok.com/search_users, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/tiktok.com/search_users

### Who maintains it?

It is part of Reduck's official curated catalogue.

### Why does TikTok user search only return about 10 accounts?

Reduck's TikTok user search returns only the first batch of accounts TikTok's website sends back, usually about 10, and in testing a request for the next page brought back nothing new. To reach more accounts, run variations of the name (add a city, a niche word or part of a handle) and merge the results on uniqueId. The get_search_suggestions script returns TikTok's autocomplete for a keyword without a sign-in, which makes a quick list of variations to rerun.

### How do I find a TikTok account's user ID or secUid from its name?

Search the name or part of the @handle: each result carries id, TikTok's numeric user ID, and secUid, the stable opaque ID other TikTok requests use to identify an account. If you already know the exact @handle, get_profile returns both IDs plus following count, video count, region and private status, and it works without being signed in to TikTok.

### How do I find TikTok creators by topic instead of by name?

Reduck's TikTok user search takes a name or part of a handle, so for a subject like sourdough or pottery it works better to start from videos. The search_videos script returns up to 300 videos for a keyword, each with its author's uniqueId; collect those handles, drop duplicates, and pass the ones worth a closer look to get_profile or get_user_videos.

### What is the official way for a brand to find TikTok creators by keyword?

Brands can use the Explore creators section of TikTok One, which searches by username or by a keyword creators have posted about and filters by country or region, follower count, language and audience. TikTok's Research API does not fit this job: it is limited to academic and not-for-profit researchers independent of commercial interests, and its user info endpoint looks up a username you already know rather than searching by keyword.

Source: https://reduck.ai/explore/scripts/reduck/tiktok.com/search_users
