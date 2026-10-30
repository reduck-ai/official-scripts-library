# Request indexing of a URL in Google Search Console

Automatically request indexing of a URL in Google Search Console on search.google.com. Ask Google to crawl and index one page of a Search Console property, as URL Inspection's Request indexing does, and return Google's answer. Google first tests the page live: when the test finds an issue (for example the page answers 404), the request is rejected and `liveCoverageState` says why; otherwise Google adds the URL to its priority crawl queue. Accepted means queued, not indexed: check later with search.google.com/inspect_url. Takes 20 seconds to about 3 minutes. Google takes a limited number of requests a day per property; past it, the script fails with a message that says so. Takes the property as search.google.com/list_properties returns it, and the Google account to act as, by its number from mail.google.com/list_accounts. A URL outside the property, or an account that cannot open it, fails with a message that says so.

- Site: search.google.com
- Address: `reduck/search.google.com/submit_url`
- Updated: 2026-10-29 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/search.google.com/submit_url`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/search.google.com/submit_url
```

## Input

- `url` (string, required): The page to submit, a full URL that belongs to the property, e.g. https://example.com/pricing.
- `siteUrl` (string, required): The property, exactly as search.google.com/list_properties returns it: a URL prefix such as https://example.com/ or a Domain property such as sc-domain:example.com.
- `account` (integer, optional): Which of the browser's signed-in Google accounts to act as, by its number from mail.google.com/list_accounts. Default 0, the browser's first account.

## Output

- `url` (string, required): The URL submitted.
- `siteUrl` (string, required): The property it was submitted in.
- `accepted` (boolean, required): true: Google added the URL to its priority crawl queue. false: the live test found an issue and Google rejected the request. Queued is not indexed.
- `requestedUrl` (string | null, required): The URL Google says it queued. Null when the request was rejected.
- `liveCoverageState` (string | null, required): What Google's live test of the page found, as Search Console's help page names it: for example submitted_and_indexed, or not_found_404 for a missing page. Null when Search Console gives none.

## FAQ

### What does "Request indexing of a URL in Google Search Console" do?

Ask Google to crawl and index one page of a Search Console property, as URL Inspection's Request indexing does, and return Google's answer. Google first tests the page live: when the test finds an issue (for example the page answers 404), the request is rejected and `liveCoverageState` says why; otherwise Google adds the URL to its priority crawl queue. Accepted means queued, not indexed: check later with search.google.com/inspect_url. Takes 20 seconds to about 3 minutes. Google takes a limited number of requests a day per property; past it, the script fails with a message that says so. Takes the property as search.google.com/list_properties returns it, and the Google account to act as, by its number from mail.google.com/list_accounts. A URL outside the property, or an account that cannot open it, fails with a message that says so.

### How do I automatically request indexing of a URL in Google Search Console on search.google.com?

Ask an AI agent connected to Reduck to run reduck/search.google.com/submit_url, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/search.google.com/submit_url

### Is there a search.google.com API to request indexing of a URL in Google Search Console?

You do not need one. "Request indexing of a URL in Google Search Console" drives the real search.google.com pages in a browser, so it works whether or not search.google.com offers an API for this.

### What information do I need to provide?

Required: siteUrl, url. Optional: account.

### What does it return?

It returns url, siteUrl, accepted, requestedUrl, liveCoverageState.

### Do I need to be logged in to search.google.com?

Yes. It acts as you on search.google.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the search.google.com cookies saved by the Reduck extension.

### Does it change anything on search.google.com, or only read data?

It makes changes on search.google.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/search.google.com/submit_url, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/search.google.com/submit_url

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/search.google.com/submit_url
