# Brave search

Brave's ranked results for any query or site: check, about 20 a page, with title, link, snippet and date.

- Site: search.brave.com
- Address: `reduck/search.brave.com/search`
- Updated: 2026-10-19 (v27)
- Author: Reduck AI (reduck)

## About

In March 2025 Anthropic listed Brave Search as a subprocessor, and Simon Willison found Claude's web search citations matching Brave's results page. Brave uses its own index (it dropped Bing in 2023), so a Google ranking tells you little here. Take a docs team that moved 300 guides to /docs last month. A week later someone runs a site: query per folder, /docs/api then /docs/sdk, with country "us", pages until hasMore goes false and checks the URLs against the sitemap. Folders matter because a domain-wide query runs dry after a handful of pages. An answer flagged operatorsApplied false counts as zero found. A guide still absent gets a search on its quoted title, then goes to the companion submit_url script, which requests a recrawl but cannot promise indexing. Guides Brave has never read carry the placeholder snippet 'We cannot provide a description for this page right now'. Brave's AI answer and forum cards stay out of the output.

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/search.brave.com/search`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/search.brave.com/search
```

## Input

- `query` (string, required): Search query. The operators site:, quoted phrases and OR are honored. site:domain also covers its subdomains (site:example.com returns docs.example.com), and site:domain/path narrows to a path prefix, which is the cheapest way to slice a large site.
- `offset` (integer, optional): 0-based page index (0 is the first page, about 20 results). The pool behind one query is limited and its depth varies by query; past its end Brave re-serves earlier pages. hasMore in the output says whether a next page exists: keep paging while it is true, and dedupe on url anyway. Default 0.
- `country` (string, optional): ISO-3166 alpha-2 country whose Brave results to read, e.g. "us". When omitted, Brave answers for the country of the browser's own network location, so the same query read from two places gives two different result pages. Pass it whenever readings must be comparable across browsers, or must stand in for another reader's, such as an assistant's US-side web search.
- `exactMatch` (boolean, optional): Deprecated; has no reliable effect, because Brave may correct spellings without saying so. To search a literal string, put it in quotes in query. Default false.

## Output

- `count` (integer, required): How many results were read from this page (results.length). Not a match count. A full page has about 16 to 20.
- `query` (string, required)
- `offset` (integer, required)
- `hasMore` (boolean, required): Whether Brave offers a next page for this query. false on the last page of the pool and on an empty answer. Past the end, Brave can show an earlier page again, so dedupe on url.
- `results` (array, required): The organic web results on the page, in rank order. Empty only when Brave said so (see emptyBecause). If the script reads zero results from a page that Brave answered normally, it fails with an error and does not return an empty list.
- `emptyBecause` (string | null, required): Why results is empty, in Brave's own terms: Brave relaxed the operators, or Brave showed its no-matches banner. null when results is not empty.
- `operatorsApplied` (boolean, required): Whether Brave applied the operators in query. false means Brave found too few matches, dropped the operators and answered a relaxed query, so the results are not filtered by them. Always true for a query with no operators.
- `country` (string | null, optional): The country the results were read for, lowercased, as passed in. null when none was passed and the page is in the locale of the browser's own network location.
- `rewrittenTo` (string | null, optional): Always null. Brave tells about a rewrite only in translated text, which the script does not read. Put the query in quotes to stop Brave from rewriting it.

## Example output

Shape only: placeholder values generated from the output schema, not a real run.

```json
{
  "count": 3,
  "query": "…",
  "offset": 3,
  "country": 3,
  "hasMore": true,
  "results": [
    {
      "age": "…",
      "url": "https://example.com/item/123",
      "title": "Example",
      "snippet": "…"
    }
  ],
  "rewrittenTo": "…",
  "emptyBecause": "…",
  "operatorsApplied": true
}
```

## FAQ

### What does "Brave search" do?

Search the web on Brave, one page of results at a time, one query per run. Returns each result's title, url, snippet and date, plus the query as you sent it (not a rewritten one: see operatorsApplied for whether Brave relaxed it). An empty result list means Brave itself found nothing, and the reason is returned in emptyBecause; if the page cannot be read, the script fails with an error instead of returning an empty list.

### What information do I need to provide?

Required: query. Optional: offset, country, exactMatch.

### What does it return?

It returns count, query, offset, country, hasMore, results, rewrittenTo, emptyBecause, operatorsApplied.

### Do I need to be logged in to search.brave.com?

No. It only uses pages of search.brave.com that are reachable without signing in.

### Does it change anything on search.brave.com, or only read data?

It only reads. It looks things up on search.brave.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/search.brave.com/search, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/search.brave.com/search

### Who maintains it?

It is part of Reduck's official curated catalogue.

### How many Brave results can I get for one query?

A full page of Brave results holds about 16 to 20 organic links, and a small pool or a last page returns fewer. How deep a query goes depends on the query: in testing, a narrow site:domain/path search ended after one page of 13, while site:reduck.ai ran out at the fifth page, which re-served the third page's results. To cover a big site, split it into path-level site: queries instead of paging deeper.

### Why does the same Brave query give different results on two machines?

Without a country, Brave localizes by the connection's IP, so a Paris office and a US server get two different lists for one query. In testing, a French connection got the French App Store page and Play Store links with hl=fr, while country "us" returned the /us/ and hl=en_US versions. Pass the same two-letter code on every run you plan to compare.

### Why does a site: search on Brave return pages from other domains?

Brave quietly loosens a site: query when too few pages match it and answers with results from across the web instead. On the page this shows as a small banner saying search operators were not applied, and the output reports it as operatorsApplied false. For an indexing check, count that answer as zero pages found.

### At what volume does Brave's paid Search API beat reading the results page?

Brave's Search API charges $5 per 1,000 requests and includes a $5 monthly credit, which pays for about 1,000 queries but still needs a card on file, so for a few thousand queries a month the API is the better buy. Reading the results page suits a few dozen checks spread over an afternoon. Brave shows its captcha after about 10 rapid queries from a fresh IP and about 3 once it has throttled you, and if one click on Verify does not clear it the run stops and needs a 30 to 60 second pause.

Source: https://reduck.ai/explore/scripts/reduck/search.brave.com/search
