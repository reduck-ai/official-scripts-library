# Get Trustpilot reviewer profile

Automatically get Trustpilot reviewer profile on trustpilot.com. Get a Trustpilot reviewer's public profile by user id: display name, country, review count, lifetime stats, and their service reviews (each carries the company it's about via businessUnit). Paginated. The user id is the reviews[].consumer.id field returned by get_reviews.

- Site: trustpilot.com
- Address: `reduck/trustpilot.com/get_reviewer`
- Updated: 2026-08-14 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/trustpilot.com/get_reviewer`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/trustpilot.com/get_reviewer
```

## Input

- `userId` (string, required): Trustpilot reviewer's user id, e.g. "5d94d461636e9426c4b832fc" (the reviews[].consumer.id field from get_reviews).
- `page` (integer, optional): 1-based page of the reviewer's reviews.

## Output

- `userId` (string, required)
- `reviews` (array, required)
- `pagination` (object, required)
- `displayName` (string, required)
- `country` (string | null, optional)
- `verified` (boolean | null, optional)
- `statistics` (object | null, optional)
- `profilePicture` (string | null, optional)
- `numberOfReviews` (integer | null, optional)

## FAQ

### What does "Get Trustpilot reviewer profile" do?

Get a Trustpilot reviewer's public profile by user id: display name, country, review count, lifetime stats, and their service reviews (each carries the company it's about via businessUnit). Paginated. The user id is the reviews[].consumer.id field returned by get_reviews.

### How do I automatically get Trustpilot reviewer profile on trustpilot.com?

Ask an AI agent connected to Reduck to run reduck/trustpilot.com/get_reviewer, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/trustpilot.com/get_reviewer

### Is there a trustpilot.com API to get Trustpilot reviewer profile?

You do not need one. "Get Trustpilot reviewer profile" drives the real trustpilot.com pages in a browser, so it works whether or not trustpilot.com offers an API for this.

### What information do I need to provide?

Required: userId. Optional: page.

### What does it return?

It returns userId, country, reviews, verified, pagination, statistics, displayName, profilePicture, numberOfReviews.

### Do I need to be logged in to trustpilot.com?

No. It only uses pages of trustpilot.com that are reachable without signing in.

### Does it change anything on trustpilot.com, or only read data?

It only reads. It looks things up on trustpilot.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/trustpilot.com/get_reviewer, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/trustpilot.com/get_reviewer

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/trustpilot.com/get_reviewer
