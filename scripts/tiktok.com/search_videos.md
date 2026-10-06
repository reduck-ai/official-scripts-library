# Search TikTok videos

Automatically search TikTok videos on tiktok.com. Up to 300 videos per keyword, with caption, creator, post date, plays and likes.

- Site: tiktok.com
- Address: `reduck/tiktok.com/search_videos`
- Updated: 2026-10-05 (v1)
- Author: Reduck AI (reduck)

## About

Scroll TikTok search for a keyword and fifty videos later you still cannot say how many went up this month or which ones passed a million plays. Give it a keyword such as "cottage cheese ice cream" and a count, 30 by default and 300 at most, and you get back each video's caption, creator handle, post time, and its play, like, comment, share and save counts. A food brand checking whether a trend still has legs can pull 200 results, sort them by post time and see whether last week's videos still clear 100k plays before briefing creators. Results follow TikTok's own ranking, there is no date or region filter, and no video URL is returned, though the creator handle and video id are enough to rebuild one. It runs against a signed-in TikTok session, and a burst of runs can hit an empty response when TikTok rate limits the account.

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/tiktok.com/search_videos`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/tiktok.com/search_videos
```

## Input

- `query` (string, required): Search keyword(s).
- `count` (integer, optional): Target number of videos to collect. The script pages the search feed until this many are gathered or results run out.

## Output

- `query` (string, required)
- `videos` (array, required)
- `hasMore` (boolean, required)

## Example output

Shape only: placeholder values generated from the output schema, not a real run.

```json
{
  "query": "…",
  "videos": [
    {
      "id": "abc123",
      "desc": "…",
      "cover": "…",
      "music": "…",
      "stats": {
        "diggCount": 3.5,
        "playCount": 3.5,
        "shareCount": 3.5,
        "repostCount": 3.5,
        "collectCount": 3.5,
        "commentCount": 3.5
      },
      "author": {
        "id": "abc123",
        "secUid": "…",
        "nickname": "…",
        "uniqueId": "abc123",
        "verified": true
      },
      "duration": 3.5,
      "createTime": 3
    }
  ],
  "hasMore": true
}
```

## FAQ

### What does "Search TikTok videos" do?

Search TikTok videos by keyword, newest-relevance order, up to `count`.

### How do I automatically search TikTok videos on tiktok.com?

Ask an AI agent connected to Reduck to run reduck/tiktok.com/search_videos, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/tiktok.com/search_videos

### Is there a tiktok.com API to search TikTok videos?

You do not need one. "Search TikTok videos" drives the real tiktok.com pages in a browser, so it works whether or not tiktok.com offers an API for this.

### What information do I need to provide?

Required: query. Optional: count.

### What does it return?

It returns query, videos, hasMore.

### Do I need to be logged in to tiktok.com?

Yes. It acts as you on tiktok.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the tiktok.com cookies saved by the Reduck extension.

### Does it change anything on tiktok.com, or only read data?

Unknown: its author has not declared whether it changes anything on tiktok.com, so treat it as if it could.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/tiktok.com/search_videos, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/tiktok.com/search_videos

### Who maintains it?

It is part of Reduck's official curated catalogue.

### Can I filter results by date, country or most liked?

No. Only a keyword and a count are accepted, and videos arrive in TikTok's own order. Every video carries a post time and its play and like counts, so narrowing by date or popularity happens on your side after the run.

### Why did my search return fewer videos than I asked for?

Three causes show up in the code. The keyword can run out of matches. A results page can hold only accounts or hashtags and no videos, and the run stops there. And videos repeated across pages are removed before the list is returned. If hasMore comes back true, TikTok had more to give, so a second run or a narrower keyword may help.

### Why does a run stop with an empty body error?

TikTok sometimes answers the search request with a blank response when an account or IP has made many requests in a short time. The run stops with that error instead of returning a partial list. Wait a while or switch network, then try again.

### Can I list every video under a hashtag?

Not as a full archive. Searching the hashtag word as a keyword returns TikTok's ranked matches, up to 300, which may not include every video that carries the tag.

Source: https://reduck.ai/explore/scripts/reduck/tiktok.com/search_videos
