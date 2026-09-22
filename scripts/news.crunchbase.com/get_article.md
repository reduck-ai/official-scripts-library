# Get Crunchbase News Article

Automatically get Crunchbase News Article on news.crunchbase.com. Fetch the full text and metadata of a single Crunchbase News article by its URL.

- Site: news.crunchbase.com
- Address: `reduck/news.crunchbase.com/get_article`
- Updated: 2026-07-27 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/news.crunchbase.com/get_article`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/news.crunchbase.com/get_article
```

## Input

- `url` (string, required): Full article URL, e.g. one returned by search_news.

## Output

- `url` (string, required)
- `body` (string, required)
- `title` (string, required)
- `author` (string | null, optional)
- `summary` (string | null, optional)
- `imageUrl` (string | null, optional)
- `categories` (array, optional)
- `modifiedDate` (string | null, optional)
- `publishedDate` (string | null, optional)

## FAQ

### What does "Get Crunchbase News Article" do?

Fetch the full text and metadata of a single Crunchbase News article by its URL.

### How do I automatically get Crunchbase News Article on news.crunchbase.com?

Ask an AI agent connected to Reduck to run reduck/news.crunchbase.com/get_article, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/news.crunchbase.com/get_article

### Is there a news.crunchbase.com API to get Crunchbase News Article?

You do not need one. "Get Crunchbase News Article" drives the real news.crunchbase.com pages in a browser, so it works whether or not news.crunchbase.com offers an API for this.

### What information do I need to provide?

Required: url.

### What does it return?

It returns url, body, title, author, summary, imageUrl, categories, modifiedDate, publishedDate.

### Do I need to be logged in to news.crunchbase.com?

No. It only uses pages of news.crunchbase.com that are reachable without signing in.

### Does it change anything on news.crunchbase.com, or only read data?

Unknown: its author has not declared whether it changes anything on news.crunchbase.com, so treat it as if it could.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/news.crunchbase.com/get_article, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/news.crunchbase.com/get_article

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/news.crunchbase.com/get_article
