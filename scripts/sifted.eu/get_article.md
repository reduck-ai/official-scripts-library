# Get Sifted Article

Automatically get Sifted Article on sifted.eu. Fetch the text and metadata of a single Sifted article by its URL. Pro-only articles return just the teaser paragraph, with isPaywalled set to true.

- Site: sifted.eu
- Address: `reduck/sifted.eu/get_article`
- Updated: 2026-07-27 (v4)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/sifted.eu/get_article`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/sifted.eu/get_article
```

## Input

- `url` (string, required): Full article URL, e.g. one returned by search_news.

## Output

- `url` (string, required)
- `body` (string, required)
- `title` (string, required)
- `isPaywalled` (boolean, required)
- `author` (string | null, optional)
- `summary` (string | null, optional)
- `category` (string | null, optional)
- `imageUrl` (string | null, optional)
- `publishedDate` (string | null, optional)

## FAQ

### What does "Get Sifted Article" do?

Fetch the text and metadata of a single Sifted article by its URL. Pro-only articles return just the teaser paragraph, with isPaywalled set to true.

### How do I automatically get Sifted Article on sifted.eu?

Ask an AI agent connected to Reduck to run reduck/sifted.eu/get_article, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/sifted.eu/get_article

### Is there a sifted.eu API to get Sifted Article?

You do not need one. "Get Sifted Article" drives the real sifted.eu pages in a browser, so it works whether or not sifted.eu offers an API for this.

### What information do I need to provide?

Required: url.

### What does it return?

It returns url, body, title, author, summary, category, imageUrl, isPaywalled, publishedDate.

### Do I need to be logged in to sifted.eu?

No. It only uses pages of sifted.eu that are reachable without signing in.

### Does it change anything on sifted.eu, or only read data?

Unknown: its author has not declared whether it changes anything on sifted.eu, so treat it as if it could.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/sifted.eu/get_article, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/sifted.eu/get_article

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/sifted.eu/get_article
