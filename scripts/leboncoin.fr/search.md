# Search Leboncoin ads

Automatically search Leboncoin ads on leboncoin.fr. Up to 35 ads per call, each with price, city, zipcode, seller type, publication date and link.

- Site: leboncoin.fr
- Address: `reduck/leboncoin.fr/search`
- Updated: 2026-10-05 (v6)
- Author: Reduck AI (reduck)

## About

Each call reads one leboncoin results page for a keyword, a list of cities, or both, and returns its ads with price_eur, zipcode, seller_type (private or pro) and published_at. Say you are after a used road bike in Lyon or Villeurbanne. Search "vélo route" with both cities in locations (there is no radius setting, so you name the towns yourself) and read pages 1 to 3, one call each. Keep category_name "Vélos", since a bike keyword also pulls in Sport & Plein air listings, then drop pro sellers and anything above 600 euros. Cards carry no description, so send the dozen url values left to get_ad for descriptions and frame sizes, and pass its seller_profile_url to get_seller_profile to see how long each seller has been on the site. If leboncoin serves a consent wall or a bot check instead of results, the run stops with an error saying so, not an empty list you could mistake for zero matches.

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/leboncoin.fr/search`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/leboncoin.fr/search
```

## Input

- `page` (integer, optional): Page index (capped at max_pages=100).
- `text` (string, optional): Free-text query, e.g. 'iphone 13' or 'table en chêne'. The aliases query, keyword and keywords are accepted for the same thing; pass whichever you have.
- `query` (string, optional): Alias for text. Accepted because it is a common name for a search term; it behaves identically.
- `keyword` (string, optional): Alias for text. Accepted because it is a common name for a search term; it behaves identically.
- `keywords` (string, optional): Alias for text. Accepted because it is a common name for a search term; it behaves identically.
- `locations` (any, optional): City name, a comma-separated list of cities, or an array of city names, e.g. 'Paris', 'Paris,Lyon' or ['Paris','Lyon']. An empty array counts as no location filter.

## Output

- `ads` (array, required)
- `count` (integer, required)
- `total` (integer, required)
- `max_pages` (integer, required)

## Example output

Shape only: placeholder values generated from the output schema, not a real run.

```json
{
  "ads": [
    {
      "id": "abc123",
      "url": "https://example.com/item/123",
      "city": "…",
      "title": "Example",
      "zipcode": "…",
      "currency": "…",
      "price_eur": 3.5,
      "thumb_url": "https://example.com/item/123",
      "category_id": "abc123",
      "image_count": 3,
      "seller_type": "…",
      "published_at": "2026-01-15T09:30:00Z",
      "category_name": "…"
    }
  ],
  "count": 3,
  "total": 3,
  "max_pages": 3
}
```

## FAQ

### What does "Search Leboncoin ads" do?

Search Leboncoin classifieds by keyword and/or location. Returns total, max_pages, count, and ads (each with id, url, title, price_eur, currency, city, zipcode, category_id, category_name, seller_type, published_at, thumb_url, image_count). Paging is capped at max_pages=100.

### How do I automatically search Leboncoin ads on leboncoin.fr?

Ask an AI agent connected to Reduck to run reduck/leboncoin.fr/search, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/leboncoin.fr/search

### Is there a leboncoin.fr API to search Leboncoin ads?

You do not need one. "Search Leboncoin ads" drives the real leboncoin.fr pages in a browser, so it works whether or not leboncoin.fr offers an API for this.

### What information do I need to provide?

Optional: page, text, query, keyword, keywords, locations.

### What does it return?

It returns ads, count, total, max_pages.

### Do I need to be logged in to leboncoin.fr?

No. It only uses pages of leboncoin.fr that are reachable without signing in.

### Does it change anything on leboncoin.fr, or only read data?

It only reads. It looks things up on leboncoin.fr and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/leboncoin.fr/search, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/leboncoin.fr/search

### Who maintains it?

It is part of Reduck's official curated catalogue.

### How many leboncoin ads can I get from one search?

The leboncoin search script returns one page of up to 35 ads per call, and leboncoin stops at page 100, so one keyword and city combination tops out at 3,500 ads. A broad search like "vélo" reported 1,380,641 matches in a September 2026 run, so most of them are out of reach. Ask for a page past the end and the error tells you how many pages the search really has.

### Can I filter leboncoin search results by price, category or newest first?

The leboncoin search script has no price, category, radius or sort input, and passing one (or a limit) fails with a validation error instead of being quietly ignored. Results come back in leboncoin's default relevance order, so a 2024 ad can sit on page 1 next to one posted the evening before. Filter on price_eur and category_name in your own code, but sorting by published_at only gives a true newest-first list when max_pages comes back under 100 and you fetch every page.

### How is this different from leboncoin's saved-search alerts?

Leboncoin lets a signed-in account save up to 50 searches and sends an email or app notification when a new matching ad is published. If all you want is a ping when a cheap bike turns up, use those. The leboncoin search script is for when you want the ads as rows with ids you can store and compare between runs, which only catches every new ad when the search is small enough to fetch in full.

### Can I search leboncoin job offers with it?

For leboncoin's Offres d'emploi category, the search_jobs script is the better fit: it returns salary, contract type, sector and experience level when the poster filled them in, and the general search script never reads those fields. It also checks the city you give against leboncoin's own city list and stops with an error on a name it cannot match.

Source: https://reduck.ai/explore/scripts/reduck/leboncoin.fr/search
