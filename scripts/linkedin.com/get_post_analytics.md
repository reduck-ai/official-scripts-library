# Get LinkedIn post analytics

Automatically get LinkedIn post analytics on linkedin.com. Read a LinkedIn post's own analytics from the post-summary page: impressions, members reached, profile viewers, followers gained, the engagement breakdown (reactions, comments, reposts, saves, sends, and link visits), and the default top-demographics bucket per category. Analytics exist only for posts the signed-in member authored, so the post must be your own — it throws otherwise. Pairs with get_profile_posts: pass the urn it returns. Older or low-reach posts legitimately lack some metrics (membersReached null) and demographics (topDemographics []). Use get_post for public counts on any post.

- Site: linkedin.com
- Address: `reduck/linkedin.com/get_post_analytics`
- Updated: 2026-09-24 (v11)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/linkedin.com/get_post_analytics`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/linkedin.com/get_post_analytics
```

## Input

- `postUrl` (string, required): The post identity: a urn (urn:li:activity:<id>, e.g. from get_profile_posts), a /feed/update/urn:li:activity:<id>/ URL, a /posts/<slug>-<id>-<code>/ permalink, a lnkd.in shortened share link, or a bare numeric activity id. Must be a post authored by the logged-in account.

## Output

- `urn` (string, required): The activity/ugcPost urn the analytics were read for (join key with get_profile_posts).
- `analyticsUrl` (string, required)
- `topDemographics` (array, required): Default 'All' view: the top bucket per available category (Location, Seniority, Company size, Industry, Job title, Company). [] when demographics are unavailable for the post.
- `saves` (number | null, optional)
- `sends` (number | null, optional): Sends on LinkedIn (DM shares).
- `reposts` (number | null, optional)
- `comments` (number | null, optional)
- `reactions` (number | null, optional)
- `linkVisits` (number | null, optional): Visits to links from this post.
- `impressions` (number | null, optional)
- `membersReached` (number | null, optional): Unique members reached; read deterministically off the page's own membersReachedFeature container, not the LLM. null on older posts that predate this metric.
- `profileViewers` (number | null, optional): Profile viewers attributed to this post.
- `followersGained` (number | null, optional)
- `linkEngagements` (number | null, optional): Total link engagements; null when the post has no link.
- `socialEngagements` (number | null, optional): Total social engagements = reactions + comments + reposts + saves + sends.

## FAQ

### What does "Get LinkedIn post analytics" do?

Read a LinkedIn post's own analytics from the post-summary page: impressions, members reached, profile viewers, followers gained, the engagement breakdown (reactions, comments, reposts, saves, sends, and link visits), and the default top-demographics bucket per category. Analytics exist only for posts the signed-in member authored, so the post must be your own — it throws otherwise. Pairs with get_profile_posts: pass the urn it returns. Older or low-reach posts legitimately lack some metrics (membersReached null) and demographics (topDemographics []). Use get_post for public counts on any post.

### How do I automatically get LinkedIn post analytics on linkedin.com?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/get_post_analytics, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/get_post_analytics

### Is there a linkedin.com API to get LinkedIn post analytics?

You do not need one. "Get LinkedIn post analytics" drives the real linkedin.com pages in a browser, so it works whether or not linkedin.com offers an API for this.

### What information do I need to provide?

Required: postUrl.

### What does it return?

It returns urn, saves, sends, reposts, comments, reactions, linkVisits, impressions, analyticsUrl, membersReached, profileViewers, followersGained, linkEngagements, topDemographics, socialEngagements.

### Do I need to be logged in to linkedin.com?

Yes. It acts as you on linkedin.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the linkedin.com cookies saved by the Reduck extension.

### Does it change anything on linkedin.com, or only read data?

It only reads. It looks things up on linkedin.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/get_post_analytics, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/get_post_analytics

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/linkedin.com/get_post_analytics
