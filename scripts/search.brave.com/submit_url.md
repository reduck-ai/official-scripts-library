# Submit URL to Brave

Automatically submit URL to Brave on search.brave.com. One URL per call, no site verification, and you get the form's verdict with its exact message.

- Site: search.brave.com
- Address: `reduck/search.brave.com/submit_url`
- Updated: 2026-10-05 (v2)
- Author: Reduck AI (reduck)

## About

Brave Search runs its own index and has no webmaster console, so this form (on the search engine, not in the Brave browser) is how a site owner asks the crawler to fetch a URL. You send one address and get back the form's verdict. Acceptance only means the request was queued. Fast submissions can trigger a bot check that ends the run with an error (on the search pages, which seem to share the same per-IP limit, it appeared after about ten rapid requests), so wait 30 to 60 seconds when that happens. Say a docs team publishes 12 pages under /docs on a Monday. They submit the eight that matter most, the other four after lunch, and a few days later run the Brave search script on site:example.com/docs. Count a page as in only when that search returns operatorsApplied as true, because with too few matches the engine drops the site: filter and returns unrelated hits.

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/search.brave.com/submit_url`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/search.brave.com/submit_url
```

## Input

- `url` (string, required): The absolute URL to submit for re-fetching, e.g. 'https://reduck.ai/pricing'. Brave validates it and rejects anything it doesn't parse as a URL (returned as accepted:false, not an error). One URL per call — the form takes exactly one.

## Output

- `url` (string, required): The URL that was submitted, echoed back from the args.
- `detail` (string | null, required): The panel's explanatory line, verbatim ('Thank you for your submission.' / 'Please insert a valid URL.'). This is where Brave states WHY a submission was rejected. null when the panel has no detail row — kept nullable because only the success and invalid-URL variants have been observed.
- `heading` (string, required): The outcome panel's heading, verbatim as rendered ('Success' / 'Error'). Localized by Brave, so branch on `accepted` instead. Required and non-empty on purpose: Brave shows a 'Verifying you're a human being' step in the SAME panel before deciding, and that intermediate state has no heading — so a missing one means the script read the panel before the verdict existed, which must fail loudly rather than validate as a successful submission.
- `accepted` (boolean, required): Whether Brave accepted the submission: true = the success panel, false = the error panel (e.g. a malformed URL). Read off the panel's own `error` class, not its wording, so it survives localization. Acceptance is a queued re-fetch request only — it carries no promise that the page gets crawled, indexed or ranked.

## Example output

Shape only: placeholder values generated from the output schema, not a real run.

```json
{
  "url": "https://example.com/item/123",
  "detail": "…",
  "heading": "…",
  "accepted": true
}
```

## FAQ

### What does "Submit URL to Brave" do?

Submit one URL to Brave Search to be re-crawled, and return the outcome Brave gave: whether it was accepted, plus Brave's own heading and message. Acceptance means Brave took the submission — not that the page was crawled, indexed or ranked. An invalid URL comes back as a rejection with Brave's message rather than as an error. Brave sometimes shows a rate-limit challenge here; if it does, the script raises an error — wait 30-60 seconds before retrying.

### How do I automatically submit URL to Brave on search.brave.com?

Ask an AI agent connected to Reduck to run reduck/search.brave.com/submit_url, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/search.brave.com/submit_url

### Is there a search.brave.com API to submit URL to Brave?

You do not need one. "Submit URL to Brave" drives the real search.brave.com pages in a browser, so it works whether or not search.brave.com offers an API for this.

### What information do I need to provide?

Required: url.

### What does it return?

It returns url, detail, heading, accepted.

### Do I need to be logged in to search.brave.com?

No. It only uses pages of search.brave.com that are reachable without signing in.

### Does it change anything on search.brave.com, or only read data?

It makes changes on search.brave.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/search.brave.com/submit_url, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/search.brave.com/submit_url

### Who maintains it?

It is part of Reduck's official curated catalogue.

### Can I submit a sitemap or my whole website to Brave Search?

There is no sitemap upload: the form takes one URL per submission, and Brave is not on IndexNow's list of participating search engines, so IndexNow plugins do not reach it either. For a new site, submit the homepage and a handful of key pages rather than every URL, because rapid submissions can trip a bot check and no pace is known to be safe.

### How long after submitting does a page show up in Brave Search?

Brave publishes no timeframe for crawling a submitted URL; the 1 to 3 days often quoted comes from a user reply on Brave's community forum, not from its staff. When you search for the page, a result whose snippet reads "We cannot provide a description for this page right now" means the engine knows the URL but has not read the page yet.

### Why would Brave not crawl a page I submitted?

Check robots.txt first: Brave's crawler help says a domain or page that Googlebot is not allowed to crawl will not be crawled by Brave's bot either. Do not expect to spot the visit in your access logs, since the crawler does not advertise a user agent of its own.

### How do I get a page removed from Brave Search?

Put a robots noindex directive on the page and submit its URL so the crawler re-fetches it, because Brave's crawler help says robots.txt is not used to keep a page out of the index. If the page is gone but still listed, submit it the same way or report it to not-found@brave.com.

Source: https://reduck.ai/explore/scripts/reduck/search.brave.com/submit_url
