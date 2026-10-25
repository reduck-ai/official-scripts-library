# Search Google News

Automatically search Google News on news.google.com. Search Google News for articles by keyword and return each result's title, source, publish time, byline and Google News article link, up to count articles. complete says whether these are all the results Google News has for the query. An empty list means the search matched nothing. Supports a recency filter (when, for example 7d) and the country and language edition. Google often refuses these searches from managed browsers, so run it on your own browser.

- Site: news.google.com
- Address: `reduck/news.google.com/search_news`
- Updated: 2026-10-22 (v6)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/news.google.com/search_news`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/news.google.com/search_news
```

## Input

- `query` (string, required): Search keywords, e.g. "anthropic". Google's search operators work here too (site:, intitle:, OR).
- `when` (string, optional): Optional recency filter, appended to the query as Google's own `when:` operator. Verified working with "1d" (past 24h, server-side filtered). Google's other documented units follow the same syntax: "1h", "7d", "1y". Note the site's own Date dropdown keeps displaying "Anytime" even when this operator is filtering — the filter is applied server-side regardless of that label. Omit for the site's inclusive "Anytime" default.
- `count` (integer, optional): Number of articles to return. Fewer come back when Google News has fewer results for the query; complete then says so.
- `country` (string, optional): Google News `gl` edition country code, e.g. "US", "FR", "JP". Combined with `language` into the site's `ceid` edition parameter.
- `language` (string, optional): Google News `hl` interface/content language, e.g. "en-US", "fr", "ja".

## Output

- `url` (string, required)
- `query` (string, required): The full query sent, including the `when:` operator if one was supplied.
- `articles` (array, required): Empty array is a legitimate outcome: Google News renders "There are no items to show." for a query with no matches. A consent interstitial or any other non-results page raises an error instead, so an empty array always means the search genuinely matched nothing.
- `articleCount` (integer, required)
- `complete` (boolean, optional): True when these are all the results Google News has for this query: it sent no further page and count cut nothing. False when count stopped the list first.
- `requestedCount` (integer, optional)

## FAQ

### What does "Search Google News" do?

Search Google News for articles by keyword and return each result's title, source, publish time, byline and Google News article link, up to count articles. complete says whether these are all the results Google News has for the query. An empty list means the search matched nothing. Supports a recency filter (when, for example 7d) and the country and language edition. Google often refuses these searches from managed browsers, so run it on your own browser.

### How do I automatically search Google News on news.google.com?

Ask an AI agent connected to Reduck to run reduck/news.google.com/search_news, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/news.google.com/search_news

### Is there a news.google.com API to search Google News?

You do not need one. "Search Google News" drives the real news.google.com pages in a browser, so it works whether or not news.google.com offers an API for this.

### What information do I need to provide?

Required: query. Optional: when, count, country, language.

### What does it return?

It returns url, query, articles, complete, articleCount, requestedCount.

### Do I need to be logged in to news.google.com?

No. It only uses pages of news.google.com that are reachable without signing in.

### Does it change anything on news.google.com, or only read data?

It only reads. It looks things up on news.google.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/news.google.com/search_news, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/news.google.com/search_news

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/news.google.com/search_news
