# Check a word against the UK trade mark register

Automatically check a word against the UK trade mark register on trademarks.ipo.gov.uk. Search the UK Intellectual Property Office's trade mark register for a word or phrase and return the marks it finds: the registration number and its page on the register, the status, the mark text as registered, the filing date, and the Nice classes it covers.

- Site: trademarks.ipo.gov.uk
- Address: `reduck/trademarks.ipo.gov.uk/check_trademark`
- Updated: 2026-09-18 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/trademarks.ipo.gov.uk/check_trademark`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/trademarks.ipo.gov.uk/check_trademark
```

## Input

- `query` (string, required): The word or phrase to look for in the mark text, e.g. "GUINNESS" or "blue ocean".
- `count` (integer, optional): How many marks to collect. The register shows ten per page, so a larger count walks on through further pages and stops when the results run out.
- `match` (string, optional): How the mark text must match: SIMILAR is the register's own default and includes near matches; EXACT is the whole mark text only; STARTSWITH, CONTAINSWORD and CONTAINSSTRING are the register's prefix, whole-word and substring options.
- `classes` (array, optional): Restrict to these Nice classes of goods and services (1-45). Omitted searches every class.
- `match_words` (string, optional): For a multi-word query, whether a mark must contain all the words or any of them. Has no effect on a single word.

## Output

- `marks` (array, required)
- `match` (string, required)
- `query` (string, required)
- `returned` (integer, required)
- `totalFound` (integer, required): How many marks the register reports for this search in total, which is usually more than were collected.
- `resultsSummary` (string | null, optional): The register's own summary line, which also gives the date range the matches were filed in.

## FAQ

### What does "Check a word against the UK trade mark register" do?

Search the UK Intellectual Property Office's trade mark register for a word or phrase and return the marks it finds: the registration number and its page on the register, the status, the mark text as registered, the filing date, and the Nice classes it covers.

### How do I automatically check a word against the UK trade mark register on trademarks.ipo.gov.uk?

Ask an AI agent connected to Reduck to run reduck/trademarks.ipo.gov.uk/check_trademark, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/trademarks.ipo.gov.uk/check_trademark

### Is there a trademarks.ipo.gov.uk API to check a word against the UK trade mark register?

You do not need one. "Check a word against the UK trade mark register" drives the real trademarks.ipo.gov.uk pages in a browser, so it works whether or not trademarks.ipo.gov.uk offers an API for this.

### What information do I need to provide?

Required: query. Optional: count, match, classes, match_words.

### What does it return?

It returns marks, match, query, returned, totalFound, resultsSummary.

### Do I need to be logged in to trademarks.ipo.gov.uk?

No. It only uses pages of trademarks.ipo.gov.uk that are reachable without signing in.

### Does it change anything on trademarks.ipo.gov.uk, or only read data?

It only reads. It looks things up on trademarks.ipo.gov.uk and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/trademarks.ipo.gov.uk/check_trademark, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/trademarks.ipo.gov.uk/check_trademark

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/trademarks.ipo.gov.uk/check_trademark
