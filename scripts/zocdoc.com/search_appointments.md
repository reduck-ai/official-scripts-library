# Search Zocdoc appointments

Automatically search Zocdoc appointments on zocdoc.com. Search Zocdoc providers and appointment availability by query and ZIP. Returns total_providers and provider cards with name, specialty, rating, review_count, address, distance_mi, sponsored, profile_url, and a 14-day availability grid of date plus slot count. Zocdoc serves roughly 22 cards per page, so page through with offset for more results.

- Site: zocdoc.com
- Address: `reduck/zocdoc.com/search_appointments`
- Updated: 2026-08-28 (v11)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/zocdoc.com/search_appointments`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/zocdoc.com/search_appointments
```

## Input

- `zip` (string, required): US ZIP code or address string accepted by zocdoc.
- `query` (string, required): Specialty, condition, or doctor name (e.g. 'Dentist', 'Primary Care Doctor', 'Dermatologist'). Resolved through Zocdoc's autocomplete to its internal specialty id; see resolved_query for the suggestion actually used.
- `gender` (string, optional): Filter providers by gender.
- `offset` (integer, optional): Pagination offset. Zocdoc serves ~22 cards per page.
- `after_5pm` (boolean, optional): Only show appointments after 5pm.
- `day_filter` (string, optional): Day-of-week / horizon filter (passthrough). Default 'AnyDay'.
- `visit_type` (string, optional): Filter by appointment modality. Defaults to any.
- `before_10am` (boolean, optional): Only show appointments before 10am.

## Output

- `providers` (array, required)
- `resolved_query` (string, required): The autocomplete suggestion the query resolved to (e.g. 'Dentist'). This is what actually filtered the results - compare it against your query.
- `total_providers` (integer | null, required): Read from window.__REDUX_STATE__.searchResults.search.searchResponse.totalCount — locale-proof, not parsed from rendered 'X providers' text.

## FAQ

### What does "Search Zocdoc appointments" do?

Search Zocdoc providers and appointment availability by query and ZIP. Returns total_providers and provider cards with name, specialty, rating, review_count, address, distance_mi, sponsored, profile_url, and a 14-day availability grid of date plus slot count. Zocdoc serves roughly 22 cards per page, so page through with offset for more results.

### How do I automatically search Zocdoc appointments on zocdoc.com?

Ask an AI agent connected to Reduck to run reduck/zocdoc.com/search_appointments, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/zocdoc.com/search_appointments

### Is there a zocdoc.com API to search Zocdoc appointments?

You do not need one. "Search Zocdoc appointments" drives the real zocdoc.com pages in a browser, so it works whether or not zocdoc.com offers an API for this.

### What information do I need to provide?

Required: query, zip. Optional: gender, offset, after_5pm, day_filter, visit_type, before_10am.

### What does it return?

It returns providers, resolved_query, total_providers.

### Do I need to be logged in to zocdoc.com?

No. It only uses pages of zocdoc.com that are reachable without signing in.

### Does it change anything on zocdoc.com, or only read data?

It only reads. It looks things up on zocdoc.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/zocdoc.com/search_appointments, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/zocdoc.com/search_appointments

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/zocdoc.com/search_appointments
