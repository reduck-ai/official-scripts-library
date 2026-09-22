# Crunchbase: Get Company News

Automatically get Company News on crunchbase.com. Recent news and press mentions for one company from Crunchbase, by permalink (title, publisher, author, URL, date). Returns the 10 most recent items; older history isn't available on the free tier.

- Site: crunchbase.com
- Address: `reduck/crunchbase.com/get_company_news`
- Updated: 2026-07-27 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/crunchbase.com/get_company_news`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/crunchbase.com/get_company_news
```

## Input

- `permalink` (string, required): Crunchbase permalink slug for the company, e.g. "qonto".

## Output

- `news` (array, required)
- `notFound` (boolean, required)
- `permalink` (string, required)
- `totalActivityCount` (number, required): Total count Crunchbase reports for this company's activity timeline (news + other tracked events); only the most recent 10 are returned below.

## FAQ

### What does "Crunchbase: Get Company News" do?

Recent news and press mentions for one company from Crunchbase, by permalink (title, publisher, author, URL, date). Returns the 10 most recent items; older history isn't available on the free tier.

### How do I automatically get Company News on crunchbase.com?

Ask an AI agent connected to Reduck to run reduck/crunchbase.com/get_company_news, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/crunchbase.com/get_company_news

### Is there a crunchbase.com API to get Company News?

You do not need one. "Crunchbase: Get Company News" drives the real crunchbase.com pages in a browser, so it works whether or not crunchbase.com offers an API for this.

### What information do I need to provide?

Required: permalink.

### What does it return?

It returns news, notFound, permalink, totalActivityCount.

### Do I need to be logged in to crunchbase.com?

Yes. It acts as you on crunchbase.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the crunchbase.com cookies saved by the Reduck extension.

### Does it change anything on crunchbase.com, or only read data?

Unknown: its author has not declared whether it changes anything on crunchbase.com, so treat it as if it could.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/crunchbase.com/get_company_news, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/crunchbase.com/get_company_news

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/crunchbase.com/get_company_news
