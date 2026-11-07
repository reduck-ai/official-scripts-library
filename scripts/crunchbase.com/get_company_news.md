# Crunchbase: Get Company News

Automatically get Company News on crunchbase.com. News articles that mention one company on Crunchbase, by permalink, newest first: title, publisher, author, URL and date, 15 per page, with the total count. Pass nextCursor as cursor for the next page; paging needs a Crunchbase Pro account, and without it the script says so. An unknown permalink is an error.

- Site: crunchbase.com
- Address: `reduck/crunchbase.com/get_company_news`
- Updated: 2026-11-06 (v7)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/crunchbase.com/get_company_news`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/crunchbase.com/get_company_news
```

## Input

- `permalink` (string, required): Crunchbase permalink slug for the company, e.g. "qonto".
- `cursor` (string, optional): nextCursor from the previous page. Leave out for the most recent news. Paging needs a Crunchbase Pro account.

## Output

- `news` (array, required)
- `permalink` (string, required)
- `nextCursor` (string | null, required): Pass as cursor to get the next page; null on the last page.
- `totalNewsCount` (number, required): Number of news items Crunchbase holds that mention this company.

## FAQ

### What does "Crunchbase: Get Company News" do?

News articles that mention one company on Crunchbase, by permalink, newest first: title, publisher, author, URL and date, 15 per page, with the total count. Pass nextCursor as cursor for the next page; paging needs a Crunchbase Pro account, and without it the script says so. An unknown permalink is an error.

### How do I automatically get Company News on crunchbase.com?

Ask an AI agent connected to Reduck to run reduck/crunchbase.com/get_company_news, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/crunchbase.com/get_company_news

### Is there a crunchbase.com API to get Company News?

You do not need one. "Crunchbase: Get Company News" drives the real crunchbase.com pages in a browser, so it works whether or not crunchbase.com offers an API for this.

### What information do I need to provide?

Required: permalink. Optional: cursor.

### What does it return?

It returns news, permalink, nextCursor, totalNewsCount.

### Do I need to be logged in to crunchbase.com?

Yes. It acts as you on crunchbase.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the crunchbase.com cookies saved by the Reduck extension.

### Does it change anything on crunchbase.com, or only read data?

Unknown: its author has not declared whether it changes anything on crunchbase.com, so treat it as if it could.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/crunchbase.com/get_company_news, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/crunchbase.com/get_company_news

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/crunchbase.com/get_company_news
