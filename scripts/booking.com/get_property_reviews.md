# Get Booking.com guest reviews

Automatically get Booking.com guest reviews on booking.com. Read the guest reviews a Booking.com property lists. Returns the property name, its overall guest score and total review count, plus each review's guest first name and country, title, score out of 10, what they liked, what they did not, the room they stayed in, the number of nights, the month of the stay, the traveller type and the date the review was written.

- Site: booking.com
- Address: `reduck/booking.com/get_property_reviews`
- Updated: 2026-09-18 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/booking.com/get_property_reviews`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/booking.com/get_property_reviews
```

## Input

- `hotel_slug` (string, required): Booking.com property path segment, e.g. "fr/hotelauroremontmartre" from booking.com/hotel/fr/hotelauroremontmartre.en-gb.html. Same value the other Booking.com scripts call hotelSlug.
- `count` (integer, optional): How many reviews to collect. The panel serves 10 per page, so a higher count steps through further pages; collection stops early when the property runs out of reviews.

## Output

- `reviews` (array, required)
- `returned` (integer, required)
- `available` (boolean, required): False when the path segment did not resolve to a property page.
- `hotel_slug` (string, required)
- `score` (number | null, optional): Overall guest score out of 10.
- `reviewCount` (integer | null, optional): Total reviews the property reports, which is normally far larger than the number returned.
- `propertyName` (string | null, optional)

## FAQ

### What does "Get Booking.com guest reviews" do?

Read the guest reviews a Booking.com property lists. Returns the property name, its overall guest score and total review count, plus each review's guest first name and country, title, score out of 10, what they liked, what they did not, the room they stayed in, the number of nights, the month of the stay, the traveller type and the date the review was written.

### How do I automatically get Booking.com guest reviews on booking.com?

Ask an AI agent connected to Reduck to run reduck/booking.com/get_property_reviews, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/booking.com/get_property_reviews

### Is there a booking.com API to get Booking.com guest reviews?

You do not need one. "Get Booking.com guest reviews" drives the real booking.com pages in a browser, so it works whether or not booking.com offers an API for this.

### What information do I need to provide?

Required: hotel_slug. Optional: count.

### What does it return?

It returns score, reviews, returned, available, hotel_slug, reviewCount, propertyName.

### Do I need to be logged in to booking.com?

No. It only uses pages of booking.com that are reachable without signing in.

### Does it change anything on booking.com, or only read data?

It only reads. It looks things up on booking.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/booking.com/get_property_reviews, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/booking.com/get_property_reviews

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/booking.com/get_property_reviews
