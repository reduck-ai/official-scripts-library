# Vinted — search item listings

Automatically search item listings on vinted.com. Up to 96 US listings a page, with size, condition, favourites and the price before and after Vinted's fee.

- Site: vinted.com
- Address: `reduck/vinted.com/search_items`
- Updated: 2026-10-05 (v6)
- Author: Reduck AI (reduck)

## About

Most people who want this flip clothes and check Vinted several times a day. Only the US catalogue at www.vinted.com is searched, so vinted.fr, vinted.de and vinted.co.uk listings are out of reach. Say you resell Levi's and search "levis 501" with order newest_first and price_to 20. Up to 96 of the newest cards come back, sometimes mostly women's cutoffs sized "XS / US 2" with the odd men's "W32" pair. Keep the W32 cards and pass their ids to get_item, since measurements tend to sit in the description, and use send_message_to_seller for anything the photos leave open. Prices arrive as display strings like "$10.00", so parse them before comparing. Results are read off Vinted's page markup, so a redesign on their side can break this until the script is updated. Vinted's own Pro Integrations API won't help: it is open only to allowlisted Pro businesses, for their own items, orders and webhooks, and has no catalogue search.

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/vinted.com/search_items`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/vinted.com/search_items
```

## Input

- `query` (string, required): Free-text search, e.g. "levis 501" or "nike air max".
- `page` (integer, optional): Result page, 96 items per page. Pages are near-disjoint but not a frozen snapshot: newly listed items shift the window, so consecutive pages fetched minutes apart can repeat a couple of items.
- `order` (string, optional): Sort order. Omit for the site default (relevance).
- `price_to` (number, optional): Maximum item price, in the currency the run's session resolves to.
- `price_from` (number, optional): Minimum item price, in the currency the run's session resolves to.

## Output

- `page` (integer, required)
- `items` (array, required)
- `search_url` (string, required)

## Example output

Shape only: placeholder values generated from the output schema, not a real run.

```json
{
  "page": 1,
  "items": [
    {
      "id": "abc123",
      "url": "https://example.com/item/123",
      "size": "…",
      "brand": "…",
      "price": "…",
      "title": "Example",
      "condition": "…",
      "image_url": "https://example.com/item/123",
      "favourites": 3,
      "total_price": 3
    }
  ],
  "search_url": "https://example.com/item/123"
}
```

## FAQ

### What does "Vinted — search item listings" do?

Search Vinted listings by keyword and return one page of results with each item's title, brand, size, condition, price, total price with Buyer Protection, favourite count, photo and link. Supports sorting, a price range and paging.

### How do I automatically search item listings on vinted.com?

Ask an AI agent connected to Reduck to run reduck/vinted.com/search_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/vinted.com/search_items

### Is there a vinted.com API to search item listings?

You do not need one. "Vinted — search item listings" drives the real vinted.com pages in a browser, so it works whether or not vinted.com offers an API for this.

### What information do I need to provide?

Required: query. Optional: page, order, price_to, price_from.

### What does it return?

It returns page, items, search_url.

### Do I need to be logged in to vinted.com?

No. It only uses pages of vinted.com that are reachable without signing in.

### Does it change anything on vinted.com, or only read data?

It only reads. It looks things up on vinted.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/vinted.com/search_items, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/vinted.com/search_items

### Who maintains it?

It is part of Reduck's official curated catalogue.

### Can it search vinted.fr, vinted.de or vinted.co.uk instead of the US site?

Not with this script: every search goes to www.vinted.com, the US site, and there is no country option. Vinted runs its US, French and UK sites as separate catalogues, so listings from vinted.fr or vinted.co.uk don't show up in these results. Prices are copied as the page displays them, so check the currency symbol if the browser runs outside the US.

### Can I use it to watch for new Vinted listings?

Run it on a schedule with order newest_first and compare ids with the previous run: any id you haven't seen before is a new listing. Each call only sees the newest 96, so on a busy query like "nike" narrow the keyword or the price range, or fresh items can slip past between runs. Paging back with page 2, 3 and so on works too, but the output carries no total count and new listings shift the window while you page, so dedupe on id.

### Does price_to include Vinted's fee or shipping?

price_to caps the item price only. Vinted's fee (usually 5% plus $0.70 on the US site) comes on top, so price_to 20 can still return a $20.00 pair of shorts whose total_price reads $21.70. Shipping is paid by the buyer at checkout and is not in total_price either, so if your budget covers everything, leave room for it.

### Can I filter Vinted results by size or brand?

Size and brand aren't search filters here. Put the brand in the query text, as in "levis 501", and filter sizes afterwards with some slack, because one search can mix "W32", "Other" and women's sizes like "XXS / US 0". Brand comes back null on unbranded listings, and size is null in categories without sizes, such as books or electronics.

Source: https://reduck.ai/explore/scripts/reduck/vinted.com/search_items
