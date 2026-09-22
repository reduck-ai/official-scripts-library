# Search Malt freelancers

Automatically search Malt freelancers on malt.com. Search Malt freelancers by keyword and city, using a Malt freelancer account (not a client/recruiter account) that is logged in. Returns the first page (up to 24) of matching profiles with rate, location, availability, rating, badges and skills. Malt may rate-limit repeated automated searches within one session, even while logged in — the script raises a clear error naming this when it happens.

- Site: malt.com
- Address: `reduck/malt.com/search_freelancers`
- Updated: 2026-09-08 (v9)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/malt.com/search_freelancers`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/malt.com/search_freelancers
```

## Input

- `query` (string, required): Free-text keyword or skill, e.g. "React developer"
- `location` (string, required): City name to search near, e.g. "London" or "Paris". The script picks the first matching city suggestion from Malt's own autocomplete.

## Output

- `profiles` (array, optional)
- `totalElements` (integer | null, optional): Total freelancers matching the query, as reported by Malt (only the first page of profiles is returned)

## FAQ

### What does "Search Malt freelancers" do?

Search Malt freelancers by keyword and city, using a Malt freelancer account (not a client/recruiter account) that is logged in. Returns the first page (up to 24) of matching profiles with rate, location, availability, rating, badges and skills. Malt may rate-limit repeated automated searches within one session, even while logged in — the script raises a clear error naming this when it happens.

### How do I automatically search Malt freelancers on malt.com?

Ask an AI agent connected to Reduck to run reduck/malt.com/search_freelancers, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/malt.com/search_freelancers

### Is there a malt.com API to search Malt freelancers?

You do not need one. "Search Malt freelancers" drives the real malt.com pages in a browser, so it works whether or not malt.com offers an API for this.

### What information do I need to provide?

Required: query, location.

### What does it return?

It returns profiles, totalElements.

### Do I need to be logged in to malt.com?

Yes. It acts as you on malt.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the malt.com cookies saved by the Reduck extension.

### Does it change anything on malt.com, or only read data?

It only reads. It looks things up on malt.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/malt.com/search_freelancers, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/malt.com/search_freelancers

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/malt.com/search_freelancers
