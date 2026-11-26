# Search Keepa Amazon price drops

Automatically search Keepa Amazon price drops on keepa.com. Search the Amazon price drops that Keepa's deals page shows to a visitor, on one of 11 Amazon countries (US, UK, Germany, France, Japan, Canada, Italy, Spain, India, Mexico, Brazil). You can set the same filters as the page: which price dropped (Amazon, Buy Box, new, new by third-party sellers, Prime exclusive, Lightning Deals, used by condition, Amazon Warehouse, refurbished, collectible), the period the drop is measured over (day, week, month, 3 months or all), words in the title, root categories to include or exclude, the drop in percent and in amount, the current price range, the lowest rating, lowest-ever and lowest-in-90-days prices, stock, reviews, Prime exclusive, whether Amazon sells the product, and the sort order. Returns one page of 150 deals: for each, the ASIN, title, Amazon link, Keepa link, image, current price, the reference price it dropped from and the average price of the period, the drop amount and percent, when the price changed and when Keepa found the deal. The first page also returns the root categories with their deal counts, whose ids the category filters take. The default filters are those of the page: Amazon price, one week, drop of 20 to 80 percent, price from 5 to 400. A search with no match returns an empty list, and a page past the last one returns an empty list with no total. Filters that need a Keepa subscription (sales rank and product attributes such as brand) are not offered.

- Site: keepa.com
- Address: `reduck/keepa.com/search_price_drops`
- Updated: 2026-11-24 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/keepa.com/search_price_drops`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/keepa.com/search_price_drops
```

## Input

- `page` (integer, optional): Result page, 150 deals a page. has_next_page says when to stop.
- `sort` (string, optional): Sort order, as the site offers it: largest drop in percent first, largest drop in amount first, lowest price first, newest deal first, or best sales rank first. sales_rank leaves out products with no sales rank.
- `query` (string, optional): Words to find in the product titles. Empty for all deals.
- `country` (string, optional): The Amazon country whose deals to search.
- `reverse` (boolean, optional): Reverse the sort order, as a second click on the sort does on the site.
- `interval` (string, optional): The period the drop is measured over: the current price is compared with the average price of the last day, week, month or 3 months. all combines the four periods.
- `price_max` (number | null, optional): Highest current price, in the country's currency. Null for no upper limit.
- `price_min` (number | null, optional): Lowest current price, in the country's currency. The site's default range is 5 to 400 (500 to 40000 yen in Japan). Null for no lower limit.
- `min_rating` (number | null, optional): Lowest average customer rating, in stars from 1 to 5. Null for any rating.
- `price_type` (string, optional): Which price dropped, as Keepa's deal types list them: the Amazon offer (the site's default), the Buy Box, the lowest new offer, new by third-party sellers shipped by Amazon (new_fba) or by the seller (new_fbm), Prime exclusive, Lightning Deals, used (any or one condition), Amazon Warehouse, refurbished or collectible.
- `has_reviews` (boolean, optional): Only products with customer reviews.
- `lowest_ever` (boolean, optional): Only products whose current price is the lowest Keepa ever recorded.
- `filter_adult` (boolean, optional): Leave out adult products, as the site does by default.
- `out_of_stock` (boolean, optional): Only products that are out of stock.
- `lowest_90_days` (boolean, optional): Only products whose current price is the lowest of the last 90 days.
- `drop_amount_max` (number | null, optional): Largest drop, in the country's currency. Null for no upper limit.
- `drop_amount_min` (number | null, optional): Smallest drop, in the country's currency. Null for no lower limit.
- `prime_exclusive` (boolean, optional): Only products with a Prime exclusive offer.
- `drop_percent_max` (integer, optional): Largest drop, in percent of the reference price.
- `drop_percent_min` (integer, optional): Smallest drop, in percent of the reference price. The site's default range is 20 to 80.
- `has_amazon_offer` (boolean | null, optional): true: only products Amazon itself sells; false: only products Amazon does not sell; null: both. Has no effect when price_type is amazon.
- `lowest_new_offer` (boolean, optional): Only deals where this price is the lowest new offer.
- `exclude_categories` (array, optional): Leave out deals in these root categories, by the ids in the categories field of an earlier first-page answer for the same country.
- `include_categories` (array, optional): Show only deals in these root categories, by the ids in the categories field of an earlier first-page answer for the same country.
- `warehouse_conditions` (array, optional): For warehouse deals, the item conditions to show.
- `one_variation_per_product` (boolean, optional): Show one variation (size, color) per product, as the site does by default.
- `drop_amount_last_change_only` (boolean, optional): Apply the drop amount range to the last price change only, not to the drop from the reference price.

## Output

- `page` (integer, required)
- `items` (array, required): The deals of this page, in the order of the sort.
- `country` (string, required)
- `currency` (string, required): ISO 4217 code of the prices.
- `per_page` (integer, required)
- `categories` (array, required): Root categories of the matching deals, with how many deals each has. Keepa sends them with the first page only: empty on later pages. Pass an id in include_categories or exclude_categories.
- `price_type` (string, required)
- `has_next_page` (boolean, required)
- `total_results` (integer | null, required): Number of deals that match, over all pages. Null on a page past the last one.

## FAQ

### What does "Search Keepa Amazon price drops" do?

Search the Amazon price drops that Keepa's deals page shows to a visitor, on one of 11 Amazon countries (US, UK, Germany, France, Japan, Canada, Italy, Spain, India, Mexico, Brazil). You can set the same filters as the page: which price dropped (Amazon, Buy Box, new, new by third-party sellers, Prime exclusive, Lightning Deals, used by condition, Amazon Warehouse, refurbished, collectible), the period the drop is measured over (day, week, month, 3 months or all), words in the title, root categories to include or exclude, the drop in percent and in amount, the current price range, the lowest rating, lowest-ever and lowest-in-90-days prices, stock, reviews, Prime exclusive, whether Amazon sells the product, and the sort order. Returns one page of 150 deals: for each, the ASIN, title, Amazon link, Keepa link, image, current price, the reference price it dropped from and the average price of the period, the drop amount and percent, when the price changed and when Keepa found the deal. The first page also returns the root categories with their deal counts, whose ids the category filters take. The default filters are those of the page: Amazon price, one week, drop of 20 to 80 percent, price from 5 to 400. A search with no match returns an empty list, and a page past the last one returns an empty list with no total. Filters that need a Keepa subscription (sales rank and product attributes such as brand) are not offered.

### How do I automatically search Keepa Amazon price drops on keepa.com?

Ask an AI agent connected to Reduck to run reduck/keepa.com/search_price_drops, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/keepa.com/search_price_drops

### Is there a keepa.com API to search Keepa Amazon price drops?

You do not need one. "Search Keepa Amazon price drops" drives the real keepa.com pages in a browser, so it works whether or not keepa.com offers an API for this.

### What information do I need to provide?

Optional: page, sort, query, country, reverse, interval, price_max, price_min, min_rating, price_type, has_reviews, lowest_ever, filter_adult, out_of_stock, lowest_90_days, drop_amount_max, drop_amount_min, prime_exclusive, drop_percent_max, drop_percent_min, has_amazon_offer, lowest_new_offer, exclude_categories, include_categories, warehouse_conditions, one_variation_per_product, drop_amount_last_change_only.

### What does it return?

It returns page, items, country, currency, per_page, categories, price_type, has_next_page, total_results.

### Do I need to be logged in to keepa.com?

No. It only uses pages of keepa.com that are reachable without signing in.

### Does it change anything on keepa.com, or only read data?

It only reads. It looks things up on keepa.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/keepa.com/search_price_drops, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/keepa.com/search_price_drops

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/keepa.com/search_price_drops
