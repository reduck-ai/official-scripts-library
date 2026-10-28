# Search Google

Automatically search Google on google.com. You get about ten organic results per page, each with its real link rather than a Google redirect.

- Site: google.com
- Address: `reduck/google.com/search_site`
- Updated: 2026-10-27 (v33)
- Author: Reduck AI (reduck)

## About

Handy when you want the list a person sees on google.com, in that order, not an index of sites you picked in advance. You type the query as you would in the search box, operators included, and can add a time window such as the past week. Back come about ten organic results from one page, with ads and the AI Overview left out. A founder hunting for a growth hire might search site:linkedin.com/in "head of growth" saas paris, fetch the first five pages and drop the duplicates. The few dozen profiles left go to the linkedin.com get_profile script, which does need a LinkedIn login. Google currently hides each result's address behind a redirect, so every link is opened in a spare tab for about 200 milliseconds to see where it lands, and that site gets the visit. If one link will not resolve within 20 seconds, the whole call fails rather than returning a list with gaps.

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/google.com/search_site`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/google.com/search_site
```

## Input

- `query` (string, required): Full Google query, e.g. 'site:linkedin.com/in Ex-UiPath' or any free-text search.
- `page` (integer, optional): Result page, 0 = first, like Google's pager (10 results per page). Different pages do not overlap, so several can be fetched at once and combined. Results are personalised to the browser's Google account and location, so the order holds only for a given account, place and moment.
- `freshness` (string, optional): Time filter: h (past hour), d (past 24h), w (past week), m (past month), y (past year), optionally with a multiplier: d2 = past 2 days, w3 = past 3 weeks, m6 = past 6 months, h5 = past 5 hours. Omit for all time.
- `sortByDate` (boolean, optional): When true, sort results by date (newest first) instead of relevance. Combines with freshness.

## FAQ

### What does "Search Google" do?

Run a Google search and return one page of organic results (title, url, site, byline, meta, snippet), with Google's link wrappers resolved to the destination url. Results can be personalized to the browser's Google account and location. Narrow queries return the same results in the same order on replay; very broad ones may reorder. For more coverage, fetch several pages or split the query (different site: paths, phrases, or freshness windows), and dedupe by url. An empty list means Google found nothing; when Google shows its anti-bot check, the run fails and says so.

### How do I automatically search Google on google.com?

Ask an AI agent connected to Reduck to run reduck/google.com/search_site, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/google.com/search_site

### Is there a google.com API to search Google?

You do not need one. "Search Google" drives the real google.com pages in a browser, so it works whether or not google.com offers an API for this.

### What information do I need to provide?

Required: query. Optional: page, freshness, sortByDate.

### Do I need to be logged in to google.com?

No. It only uses pages of google.com that are reachable without signing in.

### Does it change anything on google.com, or only read data?

It only reads. It looks things up on google.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/google.com/search_site, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/google.com/search_site

### Who maintains it?

It is part of Reduck's official curated catalogue.

### How do I get more than 10 Google results for one query?

One call returns one results page, about ten organic results, and there is no count setting, since Google stopped honouring the &num=100 trick in September 2025. To go deeper, run it again with page set to 1, 2, 3 and so on (0 is the first page), and dedupe by url because the odd result shows up twice where two pages meet. For a wide sweep, several narrower queries, one per city or per job title for example, usually turn up more distinct results than paging deep into a single one.

### What happens when Google shows a CAPTCHA or a cookie banner?

Google's cookie banner is dismissed with Reject all, so nothing optional is accepted on your behalf. If Google flags the traffic as automated and will not let the search through, the run stops with an error rather than handing back an empty list you could mistake for zero results. Runs from people's own Chrome have succeeded much more often than runs from a fresh hosted browser, so your own browser is the better place to run it.

### Can I get Google results for another country or language?

There is no country or language input, and Google's interface is pinned to English, so labels such as "2 days ago" or "750+ reactions" come back in English even for a search run from Paris. Ranking follows wherever Google thinks the browser is, judged from its IP and any Google cookies it carries, so a laptop in Lyon tends to get France-weighted results. Adding a city to the query can help, but it is not the same as searching from that country.

### Can I still sign up for Google's Custom Search JSON API?

Google's Custom Search JSON API is closed to new customers, and existing customers have until January 1, 2027 to move off it. Until then it gives 100 free queries a day and charges $5 per 1,000 after that, up to 10,000 a day, and it searches only a Programmable Search Engine you configure, with new engines limited to 50 domains. Google's suggested replacement is Vertex AI Search, which also covers up to 50 domains, and for full web search it asks you to get in touch.

Source: https://reduck.ai/explore/scripts/reduck/google.com/search_site
