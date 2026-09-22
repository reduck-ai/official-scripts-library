# Detect company's ATS (Greenhouse/Lever/Ashby)

Automatically detect company's ATS (Greenhouse/Lever/Ashby) on ats-tools. Given a company's careers page URL, detect whether it's backed by Greenhouse, Lever, or Ashby and extract the board slug usable with greenhouse.io/get_company_jobs, lever.co/get_company_jobs, or ashbyhq.com/get_company_jobs. Detection combines two signals: network requests fired by the page (Greenhouse/Lever client-side API calls, seen e.g. on discord.com/careers) and embedded links to the ATS's own hosted board (seen e.g. on notion.com/careers linking jobs.ashbyhq.com/notion). Many companies fully proxy their ATS server-side with no client-visible signal (e.g. careers.airbnb.com, retool.com/careers) - for those this returns platform: null, which is a legitimate outcome, not a failure. Point this at the company's own marketing careers page, not at a guessed ATS URL: several large companies (e.g. Airbnb, Coinbase) configure their native Greenhouse board (boards.greenhouse.io/<slug>) to redirect to their custom-branded career site, which then also yields platform: null.

- Site: ats-tools
- Address: `reduck/ats-tools/detect_ats`
- Updated: 2026-08-14 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/ats-tools/detect_ats`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/ats-tools/detect_ats
```

## Input

- `url` (string, required): URL of the company's careers/jobs page, e.g. https://discord.com/careers

## Output

- `url` (string, required)
- `slug` (string | null, required)
- `signal` (string | null, required)
- `platform` (string | null, required)

## FAQ

### What does "Detect company's ATS (Greenhouse/Lever/Ashby)" do?

Given a company's careers page URL, detect whether it's backed by Greenhouse, Lever, or Ashby and extract the board slug usable with greenhouse.io/get_company_jobs, lever.co/get_company_jobs, or ashbyhq.com/get_company_jobs. Detection combines two signals: network requests fired by the page (Greenhouse/Lever client-side API calls, seen e.g. on discord.com/careers) and embedded links to the ATS's own hosted board (seen e.g. on notion.com/careers linking jobs.ashbyhq.com/notion). Many companies fully proxy their ATS server-side with no client-visible signal (e.g. careers.airbnb.com, retool.com/careers) - for those this returns platform: null, which is a legitimate outcome, not a failure. Point this at the company's own marketing careers page, not at a guessed ATS URL: several large companies (e.g. Airbnb, Coinbase) configure their native Greenhouse board (boards.greenhouse.io/<slug>) to redirect to their custom-branded career site, which then also yields platform: null.

### How do I automatically detect company's ATS (Greenhouse/Lever/Ashby) on ats-tools?

Ask an AI agent connected to Reduck to run reduck/ats-tools/detect_ats, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/ats-tools/detect_ats

### Is there a ats-tools API to detect company's ATS (Greenhouse/Lever/Ashby)?

You do not need one. "Detect company's ATS (Greenhouse/Lever/Ashby)" drives the real ats-tools pages in a browser, so it works whether or not ats-tools offers an API for this.

### What information do I need to provide?

Required: url.

### What does it return?

It returns url, slug, signal, platform.

### Do I need to be logged in to ats-tools?

No. It only uses pages of ats-tools that are reachable without signing in.

### Does it change anything on ats-tools, or only read data?

Unknown: its author has not declared whether it changes anything on ats-tools, so treat it as if it could.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/ats-tools/detect_ats, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/ats-tools/detect_ats

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/ats-tools/detect_ats
