# Search Lands' End products

Automatically search Lands' End products on landsend.com. Search Lands' End (landsend.com, US) products by keywords, 96 a page, in the order the site gives: number, name, link, price and regular price in US dollars, image and colors of each, plus the total count and the number of pages. The site's search also returns close matches, so keywords that match nothing exactly can still give products. A page past the last one gives an empty list. When Lands' End sends the keywords to another page instead of results, redirected_to gives that page.

- Site: landsend.com
- Address: `reduck/landsend.com/search-products`
- Updated: 2026-11-27 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/landsend.com/search-products`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/landsend.com/search-products
```

## Input

- `query` (string, required): Keywords, for example "flannel shirt".
- `page` (integer, optional): Results page, 96 products a page.

## Output

- `page` (integer, required)
- `pages` (integer | null, required): Number of result pages.
- `query` (string, required)
- `total` (integer | null, required): Number of products that match, on all pages.
- `products` (array, required)
- `redirected_to` (string | null, required): The page Lands' End sent these keywords to, when it is not a search results page.

## FAQ

### What does "Search Lands' End products" do?

Search Lands' End (landsend.com, US) products by keywords, 96 a page, in the order the site gives: number, name, link, price and regular price in US dollars, image and colors of each, plus the total count and the number of pages. The site's search also returns close matches, so keywords that match nothing exactly can still give products. A page past the last one gives an empty list. When Lands' End sends the keywords to another page instead of results, redirected_to gives that page.

### How do I automatically search Lands' End products on landsend.com?

Ask an AI agent connected to Reduck to run reduck/landsend.com/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/landsend.com/search-products

### Is there a landsend.com API to search Lands' End products?

You do not need one. "Search Lands' End products" drives the real landsend.com pages in a browser, so it works whether or not landsend.com offers an API for this.

### What information do I need to provide?

Required: query. Optional: page.

### What does it return?

It returns page, pages, query, total, products, redirected_to.

### Do I need to be logged in to landsend.com?

No. It only uses pages of landsend.com that are reachable without signing in.

### Does it change anything on landsend.com, or only read data?

It only reads. It looks things up on landsend.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/landsend.com/search-products, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/landsend.com/search-products

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/landsend.com/search-products
