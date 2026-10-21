# Search eBay listings

Automatically search eBay listings on ebay.com. One page of active listings (about 60) with price, shipping cost and the seller's feedback score for each.

- Site: ebay.com
- Address: `reduck/ebay.com/search_listings`
- Updated: 2026-10-20 (v9)
- Author: Reduck AI (reduck)

## About

The job it does best is pricing something before you list it. Say a Canon AE-1 Program turned up in a drawer: search "canon ae-1 program body" and you get the active listings eBay shows for it, each with price, shipping cost and seller feedback. Add shippingCost to price for a rough landed cost before tax (shippingCost is null when a card has no delivery line). Then drop anything marked "for parts" or bundled with a lens, and send the closest body-only matches to get_listing for condition and photos. The catch is that nothing here has sold yet. A Buy It Now price is what a seller hopes to get and an auction bid will probably still climb, so check the buying-format line in attributes before trusting a number. Keywords are the only input, with no condition or price filter. Items eBay tacks on as "matching fewer words" go to relatedResults, kept apart from the real matches.

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/ebay.com/search_listings`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/ebay.com/search_listings
```

## Input

- `query` (string, required): Search keywords, e.g. "vintage camera"
- `page` (integer, optional): Result page, as eBay's own pager numbers it (1 = first page).
- `sold` (boolean, optional): Only items that sold (eBay's "Sold Items").
- `sort` (string, optional): Sort order, the options of eBay's sort menu.
- `deals` (boolean, optional): Only eBay's "Deals & Savings" listings.
- `perPage` (integer, optional): Listings per page; eBay offers 60, 120 or 240.
- `maxPrice` (number, optional): Highest item price, in the site's currency.
- `minPrice` (number, optional): Lowest item price, in the site's currency.
- `completed` (boolean, optional): Only listings that ended (eBay's "Completed Items").
- `condition` (array, optional): Keep only these item conditions. Omit for any condition.
- `freeReturns` (boolean, optional): Only listings with free returns.
- `buyingFormat` (string, optional): eBay's buying-format filter.
- `returnsAccepted` (boolean, optional): Only listings that accept returns.
- `authorizedSeller` (boolean, optional): Only authorized sellers.

## Output

- `query` (string, required)
- `results` (array, required): Listings eBay returned as matches for the query.
- `emptyReason` (string | null, required): When the results are empty and eBay says why (e.g. its notice asking for more details in the query), that notice, verbatim. null when there are results or eBay gave no reason.
- `returned` (integer, optional): How many matching listings this page yielded, excluding the loosely-related ones.
- `relatedResults` (array, optional): Listings eBay appended when the query ran out of matches. They are not results for the query and are kept apart so they cannot be mistaken for matches; usually empty.
- `resultCountText` (string | null, optional): eBay's own count heading, verbatim ("130,000+ results for vintage camera"). It is the site's total for the query, while the script reads one page.

## Example output

Shape only: placeholder values generated from the output schema, not a real run.

```json
{
  "query": "…",
  "results": [
    {
      "price": 3.5,
      "title": "Example",
      "itemId": "abc123",
      "currency": "…",
      "attributes": [
        "…"
      ],
      "shippingCost": 3.5,
      "sellerFeedbackCount": 3,
      "sellerFeedbackPercent": 3.5
    }
  ],
  "returned": 3,
  "emptyReason": "…",
  "relatedResults": [
    {
      "price": 3.5,
      "title": "Example",
      "itemId": "abc123",
      "currency": "…",
      "attributes": [
        "…"
      ],
      "shippingCost": 3.5,
      "sellerFeedbackCount": 3,
      "sellerFeedbackPercent": 3.5
    }
  ],
  "resultCountText": "…"
}
```

## FAQ

### What does "Search eBay listings" do?

Search eBay (ebay.com) for items by keyword, one page at a time: item id, title, price, currency, shipping cost, the card's attribute lines and seller feedback. No login required. Filters: sort, condition (new/used/not specified), min/max price, buying format (auction, Buy It Now, accepts offers), free returns, returns accepted, authorized sellers, sold or completed items, deals. Brand and other category-specific filters and local pickup are not offered. Pass page 2, 3, ... for later pages and perPage (60/120/240) for page size; resultCountText is eBay's total. When nothing matches, results is empty and emptyReason carries eBay's own notice when it gives one (e.g. a too-short query), otherwise null. Listings eBay pads a short result with are returned apart in relatedResults.

### How do I automatically search eBay listings on ebay.com?

Ask an AI agent connected to Reduck to run reduck/ebay.com/search_listings, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/ebay.com/search_listings

### Is there a ebay.com API to search eBay listings?

You do not need one. "Search eBay listings" drives the real ebay.com pages in a browser, so it works whether or not ebay.com offers an API for this.

### What information do I need to provide?

Required: query. Optional: page, sold, sort, deals, perPage, maxPrice, minPrice, completed, condition, freeReturns, buyingFormat, returnsAccepted, authorizedSeller.

### What does it return?

It returns query, results, returned, emptyReason, relatedResults, resultCountText.

### Do I need to be logged in to ebay.com?

No. It only uses pages of ebay.com that are reachable without signing in.

### Does it change anything on ebay.com, or only read data?

It only reads. It looks things up on ebay.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/ebay.com/search_listings, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/ebay.com/search_listings

### Who maintains it?

It is part of Reduck's official curated catalogue.

### Can it return sold or completed eBay listings?

No. It reads eBay's regular search page, which only shows items still for sale, so a price is either a Buy It Now ask or an auction's current bid, not a final sale price. eBay cut off access to its old findCompletedItems call in October 2020 and shut down the rest of the Finding API in February 2025. Its own sold-data API, Marketplace Insights, is restricted and needs eBay business approval.

### How many listings come back, and can it read page two?

One results page per run, which at eBay's default page size is about 60 listings in Best Match order (more if the browser running it has eBay set to show 120 or 240 per page). There is no page or offset input, so if eBay's heading says "130,000+ results" and you got 60, narrow the keywords until the listings you care about land on page one.

### Which price does it return for auctions or listings with several options?

On listings with variations eBay prints a range such as "$12.99 to $24.99", and price keeps the first figure, the cheapest option. On an auction it is the current bid at the moment of the search, and shipping is not added in either case: it sits separately in shippingCost.

### Does it search eBay UK, eBay.de or other eBay sites?

No, every search runs on www.ebay.com. The currency is guessed from the $, € or £ sign alone, so a Canadian "C $" price gets tagged USD, and a price in any other currency comes back with price and currency set to null.

Source: https://reduck.ai/explore/scripts/reduck/ebay.com/search_listings
