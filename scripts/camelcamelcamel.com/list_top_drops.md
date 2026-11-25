# List CamelCamelCamel top Amazon price drops

Automatically list CamelCamelCamel top Amazon price drops on camelcamelcamel.com. List the Amazon products whose price dropped the most, as CamelCamelCamel's Top Price Drops page shows them, for the Amazon country you choose (US, UK, Germany, France, Italy, Spain, Canada, Australia). Choose the view (most recent drops, or the biggest drops of the day or the week, by amount or by percent), an Amazon category and a minimum drop. Returns one page of products with ASIN, title, image, current price, the saving in percent and amount, and whether CamelCamelCamel marks it as the best price, plus whether a next page exists. Pass the ASIN to Get CamelCamelCamel Amazon price history for the full history. An empty list means no product matched.

- Site: camelcamelcamel.com
- Address: `reduck/camelcamelcamel.com/list_top_drops`
- Updated: 2026-11-24 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/camelcamelcamel.com/list_top_drops`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/camelcamelcamel.com/list_top_drops
```

## Input

- `page` (integer, optional)
- `view` (string, optional): recent (newest drops, the page's default), daily or weekly (biggest drops by amount), daily_percent or weekly_percent (biggest drops by percent).
- `country` (string, optional)
- `category` (string, optional): Amazon category as CamelCamelCamel names it in its filter, for example electronics, home-kitchen, toys-games, video-games, books. Leave out for all categories.
- `min_drop` (number, optional): Smallest drop to show: in percent for the percent views and recent, in the country's currency for daily and weekly.

## Output

- `page` (integer, required)
- `items` (array, required)
- `country` (string, required)
- `has_next_page` (boolean, required)
- `url` (string, optional)

## FAQ

### What does "List CamelCamelCamel top Amazon price drops" do?

List the Amazon products whose price dropped the most, as CamelCamelCamel's Top Price Drops page shows them, for the Amazon country you choose (US, UK, Germany, France, Italy, Spain, Canada, Australia). Choose the view (most recent drops, or the biggest drops of the day or the week, by amount or by percent), an Amazon category and a minimum drop. Returns one page of products with ASIN, title, image, current price, the saving in percent and amount, and whether CamelCamelCamel marks it as the best price, plus whether a next page exists. Pass the ASIN to Get CamelCamelCamel Amazon price history for the full history. An empty list means no product matched.

### How do I automatically list CamelCamelCamel top Amazon price drops on camelcamelcamel.com?

Ask an AI agent connected to Reduck to run reduck/camelcamelcamel.com/list_top_drops, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/camelcamelcamel.com/list_top_drops

### Is there a camelcamelcamel.com API to list CamelCamelCamel top Amazon price drops?

You do not need one. "List CamelCamelCamel top Amazon price drops" drives the real camelcamelcamel.com pages in a browser, so it works whether or not camelcamelcamel.com offers an API for this.

### What information do I need to provide?

Optional: page, view, country, category, min_drop.

### What does it return?

It returns url, page, items, country, has_next_page.

### Do I need to be logged in to camelcamelcamel.com?

No. It only uses pages of camelcamelcamel.com that are reachable without signing in.

### Does it change anything on camelcamelcamel.com, or only read data?

It only reads. It looks things up on camelcamelcamel.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/camelcamelcamel.com/list_top_drops, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/camelcamelcamel.com/list_top_drops

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/camelcamelcamel.com/list_top_drops
