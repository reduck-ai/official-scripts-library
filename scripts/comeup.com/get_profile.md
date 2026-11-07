# Get ComeUp freelancer profile

Automatically get ComeUp freelancer profile on comeup.com. Read a ComeUp seller's public profile by username: name, headline, bio, account type, positive and negative review counts, top-seller badge, response time, portfolio, and their services with price and rating. An unknown username is an error that says so.

- Site: comeup.com
- Address: `reduck/comeup.com/get_profile`
- Updated: 2026-11-06 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/comeup.com/get_profile`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/comeup.com/get_profile
```

## Input

- `username` (string, required): Seller username/slug, e.g. "guillaumetbc" (from search_freelancers' username field)

## Output

- `name` (string | null, optional)
- `headline` (string | null, optional)
- `services` (array, optional)
- `username` (string, optional)
- `portfolio` (array, optional)
- `accountType` (string | null, optional): e.g. Professionnel, Particulier
- `description` (string | null, optional)
- `isTopSeller` (boolean, optional)
- `responseTime` (string | null, optional)
- `negativeReviews` (integer | null, optional)
- `positiveReviews` (integer | null, optional)

## FAQ

### What does "Get ComeUp freelancer profile" do?

Read a ComeUp seller's public profile by username: name, headline, bio, account type, positive and negative review counts, top-seller badge, response time, portfolio, and their services with price and rating. An unknown username is an error that says so.

### How do I automatically get ComeUp freelancer profile on comeup.com?

Ask an AI agent connected to Reduck to run reduck/comeup.com/get_profile, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/comeup.com/get_profile

### Is there a comeup.com API to get ComeUp freelancer profile?

You do not need one. "Get ComeUp freelancer profile" drives the real comeup.com pages in a browser, so it works whether or not comeup.com offers an API for this.

### What information do I need to provide?

Required: username.

### What does it return?

It returns name, headline, services, username, portfolio, accountType, description, isTopSeller, responseTime, negativeReviews, positiveReviews.

### Do I need to be logged in to comeup.com?

No. It only uses pages of comeup.com that are reachable without signing in.

### Does it change anything on comeup.com, or only read data?

It only reads. It looks things up on comeup.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/comeup.com/get_profile, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/comeup.com/get_profile

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/comeup.com/get_profile
