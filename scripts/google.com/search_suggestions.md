# Get Google search suggestions

Automatically get Google search suggestions on google.com. Get the autocomplete suggestions Google offers for a search query, in the order it ranks them — the completions that would appear as you type in the search box. Partial input works well, so "best crm for" returns the ways people finish that phrase, which makes this a quick way to see what an audience actually searches for around a topic. Suggestions are personalised to the signed-in account and its location, and a query Google does not recognise comes back with an empty list rather than an error. Note that Google sometimes reinterprets an unfamiliar term and answers for a similar one, so the suggestions can drift from exactly what was asked.

- Site: google.com
- Address: `reduck/google.com/search_suggestions`
- Updated: 2026-09-22 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/google.com/search_suggestions`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/google.com/search_suggestions
```

## Input

- `query` (string, required): The partial or full search query to get suggestions for. Partial words work well — 'generative engine optimi' returns the completions Google would offer as you type.

## Output

- `query` (string, required): The query as passed in.
- `source` (string, required): Where the suggestions were read from. search_box means the endpoint was unavailable and the on-page dropdown was used instead.
- `suggestions` (array, required): The suggestions in the order Google ranks them. Empty when Google offers none for the query.
- `count` (integer, optional)
- `echoedQuery` (string | null, optional): The query as Google echoed it back, which can differ from what was sent.

## FAQ

### What does "Get Google search suggestions" do?

Get the autocomplete suggestions Google offers for a search query, in the order it ranks them — the completions that would appear as you type in the search box. Partial input works well, so "best crm for" returns the ways people finish that phrase, which makes this a quick way to see what an audience actually searches for around a topic. Suggestions are personalised to the signed-in account and its location, and a query Google does not recognise comes back with an empty list rather than an error. Note that Google sometimes reinterprets an unfamiliar term and answers for a similar one, so the suggestions can drift from exactly what was asked.

### How do I automatically get Google search suggestions on google.com?

Ask an AI agent connected to Reduck to run reduck/google.com/search_suggestions, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/google.com/search_suggestions

### Is there a google.com API to get Google search suggestions?

You do not need one. "Get Google search suggestions" drives the real google.com pages in a browser, so it works whether or not google.com offers an API for this.

### What information do I need to provide?

Required: query.

### What does it return?

It returns count, query, source, echoedQuery, suggestions.

### Do I need to be logged in to google.com?

No. It only uses pages of google.com that are reachable without signing in.

### Does it change anything on google.com, or only read data?

It only reads. It looks things up on google.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/google.com/search_suggestions, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/google.com/search_suggestions

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/google.com/search_suggestions
