# Vinted — read one item listing

Automatically read one item listing on vinted.com. Read a single Vinted listing from its link or id: title, full description, price and total with Buyer Protection, brand, size, condition, colour, material, upload time, category path, every photo, favourite count and the seller's profile.

- Site: vinted.com
- Address: `reduck/vinted.com/get_item`
- Updated: 2026-09-14 (v6)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/vinted.com/get_item`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/vinted.com/get_item
```

## Input

- `item` (string, required): The listing's full URL, or just its numeric id — e.g. "https://www.vinted.com/items/9996007247-size-12-panda-dunks" or "9996007247". Format examples only: Vinted ids are not stable over time, since listings are removed once sold or withdrawn. Pass an id you have just seen (vinted.com/search_items is the cheap way to get live ones); an id that no longer resolves is reported as such.

## Output

- `id` (string, required)
- `url` (string, required)
- `size` (string | null, optional)
- `brand` (string | null, optional)
- `price` (string | null, optional): Item price as displayed, read from the listing's own sidebar price box. Anonymous runs render the geo-default currency, not an account currency.
- `title` (string | null, optional)
- `colour` (string | null, optional)
- `photos` (array, optional)
- `seller` (object | null, optional)
- `is_sold` (boolean | null, optional): True when the listing has sold or been withdrawn; null when the page's signals disagree.
- `category` (string | null, optional)
- `currency` (string | null, optional)
- `material` (string | null, optional)
- `uploaded` (string | null, optional): Upload time as the page phrases it, e.g. "9 minutes ago".
- `condition` (string | null, optional)
- `favourites` (integer | null, optional): How many users favourited it. Null when the page renders the favourite control disabled with no count, which it does on a session-less run — that is unknown, not zero.
- `description` (string | null, optional): Null on a sold listing, which no longer carries its description anywhere readable.
- `total_price` (string | null, optional): Price including Buyer Protection, as displayed. Guaranteed >= price: that is what the field means, and the script throws rather than return a value below price, because the only way to read one is to have picked up a different listing's price node. Null if the listing's own price box no longer carries a total.
- `price_amount` (number | null, optional): Numeric item price; null on a sold listing. Only meaningful together with currency, since the site converts per session.
- `category_path` (array, optional)
- `is_favourited` (boolean | null, optional): Whether the account has favourited it; null when the run had no session, which is the default for this script.

## FAQ

### What does "Vinted — read one item listing" do?

Read a single Vinted listing from its link or id: title, full description, price and total with Buyer Protection, brand, size, condition, colour, material, upload time, category path, every photo, favourite count and the seller's profile.

### How do I automatically read one item listing on vinted.com?

Ask an AI agent connected to Reduck to run reduck/vinted.com/get_item, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/vinted.com/get_item

### Is there a vinted.com API to read one item listing?

You do not need one. "Vinted — read one item listing" drives the real vinted.com pages in a browser, so it works whether or not vinted.com offers an API for this.

### What information do I need to provide?

Required: item.

### What does it return?

It returns id, url, size, brand, price, title, colour, photos, seller, is_sold, category, currency, material, uploaded, condition, favourites, description, total_price, price_amount, category_path, is_favourited.

### Do I need to be logged in to vinted.com?

No. It only uses pages of vinted.com that are reachable without signing in.

### Does it change anything on vinted.com, or only read data?

It only reads. It looks things up on vinted.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/vinted.com/get_item, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/vinted.com/get_item

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/vinted.com/get_item
