# Get Airbnb listing reviews

Automatically get Airbnb listing reviews on airbnb.com. Read the guest reviews of one Airbnb listing by room id, one page of up to 24 at a time, in an order the reviews panel offers: most relevant, most recent, highest rated or lowest rated. Each review gives the guest's first name, the line under the name (their home town, or how long they have been on Airbnb), the star rating, the date, the trip type Airbnb highlights (for example "Stayed with kids"), the text in its original language, Airbnb's English translation when the review is in another language, and the host's response. Also returns the total number of reviews and the topics guests mention most, with their counts. Lowest rated first is the quickest way to see a listing's complaints. A page after the last review returns an empty list, and a listing with no reviews yet returns an empty list with a total of 0. A listing that does not exist or was removed fails with an error that says so.

- Site: airbnb.com
- Address: `reduck/airbnb.com/get_listing_reviews`
- Updated: 2026-10-22 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/airbnb.com/get_listing_reviews`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/airbnb.com/get_listing_reviews
```

## Input

- `id` (string, required): Airbnb room id, the number in /rooms/<id> (search_listings returns it).
- `page` (integer, optional): Page of 24 reviews. totalReviews says how many pages there are.
- `sort` (string, optional): Review order, as in the reviews panel.

## Output

- `id` (string, required)
- `page` (integer, required)
- `sort` (string, required)
- `reviews` (array, required)
- `mentions` (array, required): Topics guests mention most, as the panel lists them.
- `totalReviews` (integer, required): Reviews the listing has, as Airbnb counts them.

## FAQ

### What does "Get Airbnb listing reviews" do?

Read the guest reviews of one Airbnb listing by room id, one page of up to 24 at a time, in an order the reviews panel offers: most relevant, most recent, highest rated or lowest rated. Each review gives the guest's first name, the line under the name (their home town, or how long they have been on Airbnb), the star rating, the date, the trip type Airbnb highlights (for example "Stayed with kids"), the text in its original language, Airbnb's English translation when the review is in another language, and the host's response. Also returns the total number of reviews and the topics guests mention most, with their counts. Lowest rated first is the quickest way to see a listing's complaints. A page after the last review returns an empty list, and a listing with no reviews yet returns an empty list with a total of 0. A listing that does not exist or was removed fails with an error that says so.

### How do I automatically get Airbnb listing reviews on airbnb.com?

Ask an AI agent connected to Reduck to run reduck/airbnb.com/get_listing_reviews, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/airbnb.com/get_listing_reviews

### Is there a airbnb.com API to get Airbnb listing reviews?

You do not need one. "Get Airbnb listing reviews" drives the real airbnb.com pages in a browser, so it works whether or not airbnb.com offers an API for this.

### What information do I need to provide?

Required: id. Optional: page, sort.

### What does it return?

It returns id, page, sort, reviews, mentions, totalReviews.

### Do I need to be logged in to airbnb.com?

No. It only uses pages of airbnb.com that are reachable without signing in.

### Does it change anything on airbnb.com, or only read data?

It only reads. It looks things up on airbnb.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/airbnb.com/get_listing_reviews, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/airbnb.com/get_listing_reviews

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/airbnb.com/get_listing_reviews
