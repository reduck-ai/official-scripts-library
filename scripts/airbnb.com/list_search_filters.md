# List Airbnb search filters

Automatically list Airbnb search filters on airbnb.com. List the filters Airbnb offers for a stays search in one location, with the value each option takes: room types, amenities, property types, property tags, host languages, booking options and the neighborhoods of that location. Each filter is a key and a value that Search Airbnb listings takes as the arg of the same name. Neighborhoods are different for each location, so ask for the location you will search.

- Site: airbnb.com
- Address: `reduck/airbnb.com/list_search_filters`
- Updated: 2026-10-16 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/airbnb.com/list_search_filters`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/airbnb.com/list_search_filters
```

## Input

- `location` (string, required): Destination as a person types it, e.g. "Lisbon, Portugal". The same value you pass to search_listings.

## Output

- `filters` (array, required): One row per option. key is the search_listings arg (amenities, room_types, l2_property_type_ids, kg_and_tags, host_languages, neighborhood_ids, ib, ...); value is what to put in it.
- `location` (string, required)

## FAQ

### What does "List Airbnb search filters" do?

List the filters Airbnb offers for a stays search in one location, with the value each option takes: room types, amenities, property types, property tags, host languages, booking options and the neighborhoods of that location. Each filter is a key and a value that Search Airbnb listings takes as the arg of the same name. Neighborhoods are different for each location, so ask for the location you will search.

### How do I automatically list Airbnb search filters on airbnb.com?

Ask an AI agent connected to Reduck to run reduck/airbnb.com/list_search_filters, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/airbnb.com/list_search_filters

### Is there a airbnb.com API to list Airbnb search filters?

You do not need one. "List Airbnb search filters" drives the real airbnb.com pages in a browser, so it works whether or not airbnb.com offers an API for this.

### What information do I need to provide?

Required: location.

### What does it return?

It returns filters, location.

### Do I need to be logged in to airbnb.com?

No. It only uses pages of airbnb.com that are reachable without signing in.

### Does it change anything on airbnb.com, or only read data?

It only reads. It looks things up on airbnb.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/airbnb.com/list_search_filters, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/airbnb.com/list_search_filters

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/airbnb.com/list_search_filters
