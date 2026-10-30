# Inspect a URL in Google Search Console

Run Google Search Console's URL Inspection for one page of a property and return what Google's index holds for it: whether the URL is on Google, its coverage state as Search Console names it (for example submitted_and_indexed, crawled_currently_not_indexed, url_unknown), when Google last crawled it, the sitemaps that list it, the pages that link to it, and the canonical the page declares. Lists are empty and the last crawl is null when Google has none. Takes the property as search.google.com/list_properties returns it, and the Google account to act as, by its number from mail.google.com/list_accounts. A URL outside the property, or an account that cannot open it, fails with a message that says so.

- Site: search.google.com
- Address: `reduck/search.google.com/inspect_url`
- Updated: 2026-10-29 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/search.google.com/inspect_url`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/search.google.com/inspect_url
```

## Input

- `url` (string, required): The page to inspect, a full URL that belongs to the property, e.g. https://example.com/pricing.
- `siteUrl` (string, required): The property, exactly as search.google.com/list_properties returns it: a URL prefix such as https://example.com/ or a Domain property such as sc-domain:example.com.
- `account` (integer, optional): Which of the browser's signed-in Google accounts to act as, by its number from mail.google.com/list_accounts. Default 0, the browser's first account.

## Output

- `url` (string, required): The URL inspected.
- `siteUrl` (string, required): The property it was inspected in.
- `verdict` (string, required): on_google when Search Console says the URL is on Google, not_on_google when it says it is not; code_<n> for a verdict this script does not know yet.
- `sitemaps` (array | null, required): The sitemaps Google found the URL in. Null when Search Console gives no answer for them (a URL Google does not know, or the console's own temporary error).
- `lastCrawlAt` (string | null, required): When Google last crawled the URL, ISO 8601. Null when it never did.
- `coverageState` (string | null, required): Search Console's coverage state, as its help page names it: submitted_and_indexed, url_unknown, crawled_currently_not_indexed, and so on. Null when Search Console gives none.
- `userCanonical` (string | null, required): The canonical URL the page declares. Null when it declares none or Google has not crawled it.
- `referringPages` (array | null, required): Pages Google found linking to the URL. Null when Search Console gives no answer for them.

## FAQ

### What does "Inspect a URL in Google Search Console" do?

Run Google Search Console's URL Inspection for one page of a property and return what Google's index holds for it: whether the URL is on Google, its coverage state as Search Console names it (for example submitted_and_indexed, crawled_currently_not_indexed, url_unknown), when Google last crawled it, the sitemaps that list it, the pages that link to it, and the canonical the page declares. Lists are empty and the last crawl is null when Google has none. Takes the property as search.google.com/list_properties returns it, and the Google account to act as, by its number from mail.google.com/list_accounts. A URL outside the property, or an account that cannot open it, fails with a message that says so.

### What information do I need to provide?

Required: siteUrl, url. Optional: account.

### What does it return?

It returns url, siteUrl, verdict, sitemaps, lastCrawlAt, coverageState, userCanonical, referringPages.

### Do I need to be logged in to search.google.com?

Yes. It acts as you on search.google.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the search.google.com cookies saved by the Reduck extension.

### Does it change anything on search.google.com, or only read data?

It only reads. It looks things up on search.google.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/search.google.com/inspect_url, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/search.google.com/inspect_url

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/search.google.com/inspect_url
