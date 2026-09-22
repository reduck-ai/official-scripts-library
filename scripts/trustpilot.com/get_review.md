# Get single Trustpilot review

Automatically get single Trustpilot review on trustpilot.com. Get one Trustpilot review by its id (the review.id from get_reviews) via its permalink: author, rating, title, full text, dates, likes, verification, the company's reply, and the business it's about.

- Site: trustpilot.com
- Address: `reduck/trustpilot.com/get_review`
- Updated: 2026-08-14 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/trustpilot.com/get_review`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/trustpilot.com/get_review
```

## Input

- `reviewId` (string, required): Review id, e.g. "6a3a161deae6527cc081666d" (the id field from get_reviews).

## Output

- `id` (string, required)
- `text` (string | null, required)
- `rating` (integer, required)
- `dates` (object, optional)
- `likes` (integer | null, optional)
- `reply` (object | null, optional)
- `title` (string | null, optional)
- `source` (string | null, optional)
- `business` (object | null, optional)
- `consumer` (object | null, optional)
- `language` (string | null, optional)
- `location` (object | null, optional)
- `isVerified` (boolean, optional)

## FAQ

### What does "Get single Trustpilot review" do?

Get one Trustpilot review by its id (the review.id from get_reviews) via its permalink: author, rating, title, full text, dates, likes, verification, the company's reply, and the business it's about.

### How do I automatically get single Trustpilot review on trustpilot.com?

Ask an AI agent connected to Reduck to run reduck/trustpilot.com/get_review, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/trustpilot.com/get_review

### Is there a trustpilot.com API to get single Trustpilot review?

You do not need one. "Get single Trustpilot review" drives the real trustpilot.com pages in a browser, so it works whether or not trustpilot.com offers an API for this.

### What information do I need to provide?

Required: reviewId.

### What does it return?

It returns id, text, dates, likes, reply, title, rating, source, business, consumer, language, location, isVerified.

### Do I need to be logged in to trustpilot.com?

No. It only uses pages of trustpilot.com that are reachable without signing in.

### Does it change anything on trustpilot.com, or only read data?

It only reads. It looks things up on trustpilot.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/trustpilot.com/get_review, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/trustpilot.com/get_review

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/trustpilot.com/get_review
