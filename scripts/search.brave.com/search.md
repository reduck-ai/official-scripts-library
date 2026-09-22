# Brave search

Search the web on Brave, one page of results at a time. Returns each result's title, url, snippet and date, plus the query it actually ran.

- Site: search.brave.com
- Address: `reduck/search.brave.com/search`
- Updated: 2026-09-22 (v13)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/search.brave.com/search`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/search.brave.com/search
```

## Input

- `query` (string, required): Search query. Operators site:/""/OR are honored. NOTE `site:domain` also covers its SUBDOMAINS (site:example.com returns docs.example.com), and `site:domain/path` narrows to a path prefix — the cheapest way to slice a large site.
- `offset` (integer, optional): 0-based page index (0 = first page, ~20 results). The pool behind one query string is FINITE and its depth varies by query; past its end Brave re-serves earlier pages (measured: `site:reduck.ai` at offset 4 returned offset 2's list). `hasMore` in the output is Brave's own word on whether a next page exists — page while it is true, and dedupe on url anyway. Default 0.
- `country` (string, optional): ISO-3166 alpha-2 country whose Brave results to read, e.g. "us". Omitted, Brave answers in the country of the browser's own egress, so the same query read from two places is two different result pages (measured 2026-09-22: from France, bare = fr; `us` returns the US App Store, `hl=en_US` Play Store and `/en-en/` site pages). Pass it whenever a reading must be comparable across browsers, or must stand in for another reader's (an assistant's US-side web search).
- `exactMatch` (boolean, optional): Meant to force the literal query by clicking Brave's 'Search instead for' link. MEASURED NO-OP — do not rely on it. On three typo'd queries (2026-08-08) Brave returned results for the CORRECTED spellings while offering no such link and reporting rewrittenTo null, so the flag did nothing and said nothing about it. It can only work when Brave ANNOUNCES a rewrite, which it appears to have stopped doing for spelling corrections. To pin a literal string, quote it in `query` instead. Default false.

## Output

- `count` (integer, required): How many result cards were extracted from THIS page — literally results.length. NOT a match count and NOT an estimate of what Brave holds for the query; there is no such number on the page. A full page reads ~16-20.
- `query` (string, required)
- `offset` (integer, required)
- `hasMore` (boolean, required): Whether Brave offers a next page for this query — its pager's next-page control, enabled or disabled. false on a pool's last page and on an empty answer. This is the end-of-pool signal: page while true, dedupe on url regardless, because the last page can repeat an earlier one.
- `results` (array, required): The page's organic web results, in rank order. EMPTY ONLY WHEN BRAVE SAID SO — see `emptyBecause`. If this script reads zero rows off a page that Brave answered normally it THROWS instead of returning [], because a silent empty is indistinguishable from a real one to any schema and would be read as 'the domain has nothing on this topic'.
- `emptyBecause` (string | null, required): Why `results` is empty, in Brave's own terms — and null whenever `results` is non-empty. One of: the operators were relaxed (too few documents matched them), Brave's no-matches banner, or its no-results message. This is what makes an empty answer READABLE: an empty set is a fact about the query, never a scraper failure, because the failure case throws.
- `operatorsApplied` (boolean, required): Whether Brave honored the operators in `query`. false = Brave found too few matching documents, dropped the operators and answered a RELAXED query instead (it shows a 'search operators were not applied — Too few matches were found' banner): `results` are then soft relevance over the whole web, NOT filtered, so treat them as empty for any hard-filter use such as a site: coverage check. ONLY MEANINGFUL WHEN `query` CONTAINS AN OPERATOR — for an operator-free query it is vacuously true. Detected language-independently via the banner's /help/operators link, with the English sentence as a fallback; either signal reports false, so it errs toward warning you.
- `country` (string | null, optional): The country the results were read for, lowercased, as passed in; null when none was passed and the page is the egress's own locale.
- `rewrittenTo` (string | null, optional): What Brave actually searched if it ANNOUNCED an auto-rewrite, else null. Read off the English 'Showing results for' line, so it stays null on a localized SERP — and also, measured, when Brave silently corrects a typo and announces nothing. null therefore means 'no rewrite was announced', never 'the literal query was searched'.

## FAQ

### What does "Brave search" do?

Search the web on Brave, one page of results at a time. Returns each result's title, url, snippet and date, plus the query it actually ran.

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

Source: https://reduck.ai/explore/scripts/reduck/search.brave.com/search
