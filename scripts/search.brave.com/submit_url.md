# Submit URL to Brave

Automatically submit URL to Brave on search.brave.com. Submit one URL to Brave Search to be re-crawled, and return the outcome Brave gave: whether it was accepted, plus Brave's own heading and message. Acceptance means Brave took the submission — not that the page was crawled, indexed or ranked. An invalid URL comes back as a rejection with Brave's message rather than as an error. Brave sometimes shows a rate-limit challenge here; if it does, the script raises an error — wait 30-60 seconds before retrying.

- Site: search.brave.com
- Address: `reduck/search.brave.com/submit_url`
- Updated: 2026-08-13 (v2)
- Author: Reduck AI (reduck)

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

It makes changes on search.brave.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/search.brave.com/submit_url, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/search.brave.com/submit_url

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/search.brave.com/submit_url
