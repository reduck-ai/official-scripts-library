# Get Tripadvisor reviews

Automatically get Tripadvisor reviews on tripadvisor.com. Fetch the visible reviews for a Tripadvisor listing (restaurant, hotel, or attraction): reviewer name, rating, title, date, trip type, and review text. No login required.

- Site: tripadvisor.com
- Address: `reduck/tripadvisor.com/get_reviews`
- Updated: 2026-09-02 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/tripadvisor.com/get_reviews`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/tripadvisor.com/get_reviews
```

## Input

- `location_id` (string, required): Tripadvisor location id, the number after 'd' in the URL, e.g. "14039269" from tripadvisor.com/Restaurant_Review-g187147-d14039269-Reviews-...

## Output

- `reviews` (array, required)
- `available` (boolean, required)
- `location_id` (string, required)

## FAQ

### What does "Get Tripadvisor reviews" do?

Fetch the visible reviews for a Tripadvisor listing (restaurant, hotel, or attraction): reviewer name, rating, title, date, trip type, and review text. No login required.

### How do I automatically get Tripadvisor reviews on tripadvisor.com?

Ask an AI agent connected to Reduck to run reduck/tripadvisor.com/get_reviews, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/tripadvisor.com/get_reviews

### Is there a tripadvisor.com API to get Tripadvisor reviews?

You do not need one. "Get Tripadvisor reviews" drives the real tripadvisor.com pages in a browser, so it works whether or not tripadvisor.com offers an API for this.

### What information do I need to provide?

Required: location_id.

### What does it return?

It returns reviews, available, location_id.

### Do I need to be logged in to tripadvisor.com?

No. It only uses pages of tripadvisor.com that are reachable without signing in.

### Does it change anything on tripadvisor.com, or only read data?

It only reads. It looks things up on tripadvisor.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/tripadvisor.com/get_reviews, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/tripadvisor.com/get_reviews

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/tripadvisor.com/get_reviews
