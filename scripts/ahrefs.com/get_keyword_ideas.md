# Ahrefs API: get keyword ideas with search volume

Automatically get keyword ideas with search volume on ahrefs.com. An unofficial Ahrefs keyword API: keyword and question ideas for a seed, with monthly search volume and difficulty, free, no account. Get keyword ideas for a seed keyword from Ahrefs' free keyword generator, with each one's monthly Google search volume range and ranking difficulty in a chosen country. Returns the first 20 keywords that contain the seed, the first 20 phrased as questions, and how many of each Ahrefs knows in total. Volume comes as a range, as the free tool shows it: fewer than 100, or more than 100, 1,000, 10,000 or 100,000 searches a month. No login required. Run seeds one after another on one browser: several at once from the same browser can go unanswered.

- Site: ahrefs.com
- Address: `reduck/ahrefs.com/get_keyword_ideas`
- Updated: 2026-09-25 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/ahrefs.com/get_keyword_ideas`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/ahrefs.com/get_keyword_ideas
```

## Input

- `keyword` (string, required): The seed keyword, e.g. "apartment hunting".
- `country` (string, optional): Two-letter country code, lowercase, e.g. us, gb, fr.

## Output

- `ideas` (array, required)
- `total` (integer, required): How many keywords containing the seed Ahrefs knows; ideas holds the first 20.
- `country` (string, required)
- `keyword` (string, required)
- `questions` (array, required)
- `questionTotal` (integer, required)

## FAQ

### What does "Ahrefs API: get keyword ideas with search volume" do?

An unofficial Ahrefs keyword API: keyword and question ideas for a seed, with monthly search volume and difficulty, free, no account. Get keyword ideas for a seed keyword from Ahrefs' free keyword generator, with each one's monthly Google search volume range and ranking difficulty in a chosen country. Returns the first 20 keywords that contain the seed, the first 20 phrased as questions, and how many of each Ahrefs knows in total. Volume comes as a range, as the free tool shows it: fewer than 100, or more than 100, 1,000, 10,000 or 100,000 searches a month. No login required. Run seeds one after another on one browser: several at once from the same browser can go unanswered.

### How do I automatically get keyword ideas with search volume on ahrefs.com?

Ask an AI agent connected to Reduck to run reduck/ahrefs.com/get_keyword_ideas, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/ahrefs.com/get_keyword_ideas

### Is there a ahrefs.com API to get keyword ideas with search volume?

You do not need one. "Ahrefs API: get keyword ideas with search volume" drives the real ahrefs.com pages in a browser, so it works whether or not ahrefs.com offers an API for this.

### What information do I need to provide?

Required: keyword. Optional: country.

### What does it return?

It returns ideas, total, country, keyword, questions, questionTotal.

### Do I need to be logged in to ahrefs.com?

No. It only uses pages of ahrefs.com that are reachable without signing in.

### Does it change anything on ahrefs.com, or only read data?

It only reads. It looks things up on ahrefs.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/ahrefs.com/get_keyword_ideas, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/ahrefs.com/get_keyword_ideas

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/ahrefs.com/get_keyword_ideas
