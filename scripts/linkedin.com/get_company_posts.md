# Get LinkedIn company posts

Automatically get LinkedIn company posts on linkedin.com. You get up to the 50 newest, each with an exact post date and reaction, comment and repost counts.

- Site: linkedin.com
- Address: `reduck/linkedin.com/get_company_posts`
- Updated: 2026-10-05 (v12)
- Author: Reduck AI (reduck)

## About

Company pages on LinkedIn open on a relevance-ranked "Top" view and label posts "1w" or "1mo", so it is hard to say what a brand posted last month. The script switches the sort to Recent first and turns each activity id into an exact postedAt timestamp. The full commentary comes back, including the part LinkedIn hides behind "...more". Say you do product marketing at a small CRM company. Every Monday you run it on hubspot with count 30, throw out the isRepost rows and rank what went up in the last seven days by reactions. The top url then goes to get_post_comments to see who replied. LinkedIn's own Posts API will not read a competitor's feed, because it returns an organization's posts only to members holding an administrator, content admin or sponsored content poster role on that page. The ceiling is 50 posts with no offset, so a year of a page's history is out of reach.

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/linkedin.com/get_company_posts`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/linkedin.com/get_company_posts
```

## Input

- `company` (string, required): LinkedIn company page URL (e.g. https://www.linkedin.com/company/fintech-collective/) or bare slug (fintech-collective).
- `count` (integer, optional): How many of the most recent posts to return. Default 10 (one feed fetch); above 10 the script scroll-paginates by 10 per round. Capped at 50.

## Output

- `posts` (array, required): Newest first (ordered by activity id, which encodes the timestamp — NOT by the feed's display order).
- `total` (integer, required): Total posts on the page, from the feed module's paging metadata in the cold SSR blob. 0 with posts:[] = page has never posted ('No posts yet' state, first-class outcome).
- `company` (string, required): Slug as requested (after URL parsing).

## Example output

Shape only: placeholder values generated from the output schema, not a real run.

```json
{
  "posts": [
    {
      "age": "…",
      "url": "https://example.com/item/123",
      "text": "…",
      "reposts": 3,
      "comments": 3,
      "isRepost": true,
      "postedAt": "2026-01-15T09:30:00Z",
      "reactions": 3,
      "activityId": "abc123"
    }
  ],
  "total": 3,
  "company": "…"
}
```

## FAQ

### What does "Get LinkedIn company posts" do?

Get the most recent posts of a LinkedIn company page (newest first) from its URL or slug, up to count. Returns company, total, and posts (activityId, url, text, postedAt, age, isRepost, reactions, comments, reposts).

### How do I automatically get LinkedIn company posts on linkedin.com?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/get_company_posts, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/get_company_posts

### Is there a linkedin.com API to get LinkedIn company posts?

You do not need one. "Get LinkedIn company posts" drives the real linkedin.com pages in a browser, so it works whether or not linkedin.com offers an API for this.

### What information do I need to provide?

Required: company. Optional: count.

### What does it return?

It returns posts, total, company.

### Do I need to be logged in to linkedin.com?

Yes. It acts as you on linkedin.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the linkedin.com cookies saved by the Reduck extension.

### Does it change anything on linkedin.com, or only read data?

It only reads. It looks things up on linkedin.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/get_company_posts, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/get_company_posts

### Who maintains it?

It is part of Reduck's official curated catalogue.

### How many posts can I pull from a LinkedIn company page in one run?

The 50 newest at most, and 10 if you leave count unset. Past 10 it scrolls the feed for more, and when LinkedIn stops loading posts early you get whatever had loaded rather than an error, so a run can come back short. With no offset input, the 51st newest post and anything older stay out of reach.

### What happens if I run it on a company page I manage?

LinkedIn sends a page's admins to its admin dashboard by default, so the script asks for the member view of the page (viewAsMember=true) and navigates a second time if it still lands on the dashboard. If LinkedIn keeps redirecting, the run ends with an error naming the admin view, and running it from an account that does not manage the page gets around it.

### How do I see who reacted to or commented on one of these posts?

Pass the post's url to get_post_reactors for the people behind the reaction count, or to get_post_comments for the comment threads. On its own, get_company_posts returns only the counts and no media field; get_post can tell you whether a post carries an image, video or document, though not the file itself.

### Does it work if my LinkedIn interface is not in English?

The sort switch, the counts and the repost flag are read from page structure rather than English labels, and it has been run against Italian, Spanish, German, French and English interfaces. The age field keeps your interface's wording, so filter on postedAt instead. That one is a UTC timestamp, which means a post published just after midnight in Paris carries the previous day's date.

Source: https://reduck.ai/explore/scripts/reduck/linkedin.com/get_company_posts
