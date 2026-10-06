# Search Crunchbase News

Automatically search Crunchbase News on news.crunchbase.com. Get the newest funding and startup stories by section or keyword, with author and summary.

- Site: news.crunchbase.com
- Address: `reduck/news.crunchbase.com/search_news`
- Updated: 2026-10-05 (v4)
- Author: Reduck AI (reduck)

## About

Pick a section from the Crunchbase News nav, such as fintech, ai or public/ipo, or type a search term, and you get a page of articles from the site's RSS feeds, newest first, each with a short summary. The summary is the excerpt the editors publish in the feed, often a sentence or two, not the first paragraph of the article. A typical use is a weekly fintech check: an associate at a fund pulls page 1 of the fintech section every Monday and drops any url already in last week's sheet. Page 1 spans several weeks, so few stories are new. Headlines that name a round size go to get_article for the full text. Search matches anywhere in the article body and sorts by date, not relevance, so roundups that mention a term once also match. Dates arrive as RSS strings such as Thu, 01 Oct 2026 13:55:55 +0000, so parse them first.

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/news.crunchbase.com/search_news`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/news.crunchbase.com/search_news
```

## Input

- `page` (integer, optional): 1-based page number for pagination.
- `query` (string, optional): Full-text search query, e.g. "biotech". Mutually exclusive with section.
- `section` (string, optional): Topic section path as it appears in the site nav, e.g. "fintech", "ai", "seed", "public/ipo". Mutually exclusive with query.

## FAQ

### What does "Search Crunchbase News" do?

List recent Crunchbase News articles, either by topic section or by a search query, with pagination.

### How do I automatically search Crunchbase News on news.crunchbase.com?

Ask an AI agent connected to Reduck to run reduck/news.crunchbase.com/search_news, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/news.crunchbase.com/search_news

### Is there a news.crunchbase.com API to search Crunchbase News?

You do not need one. "Search Crunchbase News" drives the real news.crunchbase.com pages in a browser, so it works whether or not news.crunchbase.com offers an API for this.

### What information do I need to provide?

Optional: page, query, section.

### Do I need to be logged in to news.crunchbase.com?

No. It only uses pages of news.crunchbase.com that are reachable without signing in.

### Does it change anything on news.crunchbase.com, or only read data?

Unknown: its author has not declared whether it changes anything on news.crunchbase.com, so treat it as if it could.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/news.crunchbase.com/search_news, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/news.crunchbase.com/search_news

### Who maintains it?

It is part of Reduck's official curated catalogue.

### How do I page back through older articles?

Raise page by one each call. Past the last page the script returns an empty list instead of an error. Depth depends on the feed, and busy sections go back much further than quiet ones, so keep paging until you get an empty list.

### Which section names does it accept?

Any path that appears after /sections/ in the site navigation links, for example ai, cybersecurity, layoffs, public/ipo or fintech-ecommerce/crypto. A misspelled section fails on page 1 with an error naming it, rather than returning an empty list.

### Can I get the full article text, not just the summary?

The summary field is the short excerpt Crunchbase News puts in its feed, usually a sentence or two, not the article body. Pass an article's url to the sibling get_article script for news.crunchbase.com to get the body, the lead image and the last modified date.

### What comes back if Crunchbase News never mentioned the company I searched for?

An empty list, not an error. The search only covers articles Crunchbase News has published, not the Crunchbase company database, so a startup with a profile but no coverage returns nothing. For the company record itself, such as total funding and last round, the get_company_profile script on crunchbase.com takes the permalink and does not need a login.

Source: https://reduck.ai/explore/scripts/reduck/news.crunchbase.com/search_news
