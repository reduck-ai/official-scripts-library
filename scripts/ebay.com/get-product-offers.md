# Get eBay product offers from all sellers

Automatically get eBay product offers from all sellers on ebay.com. List every seller offering one eBay catalog product.

- Site: ebay.com
- Address: `reduck/ebay.com/get-product-offers`
- Updated: 2026-11-25 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/ebay.com/get-product-offers`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/ebay.com/get-product-offers
```

## Input

- `product` (string, required): eBay catalog product id (ePID, e.g. 23065742615), a product link (ebay.com/p/<ePID>) or a listing link that carries epid=.
- `page` (integer, optional): Page of the offer list, 60 offers each. has_next_page says when to stop.

## Output

- `page` (integer, required)
- `offers` (array, required): This page's listings of the product, one per seller listing, in eBay's order. Empty past the last page or for a product nobody sells.
- `productId` (string, required): The ePID read.
- `total_offers` (integer | null, required): Listings eBay counts for this product, all pages together.
- `has_next_page` (boolean, required)
- `url` (string, optional)

## FAQ

### What does "Get eBay product offers from all sellers" do?

List every seller offering one eBay catalog product.

### How do I automatically get eBay product offers from all sellers on ebay.com?

Ask an AI agent connected to Reduck to run reduck/ebay.com/get-product-offers, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/ebay.com/get-product-offers

### Is there a ebay.com API to get eBay product offers from all sellers?

You do not need one. "Get eBay product offers from all sellers" drives the real ebay.com pages in a browser, so it works whether or not ebay.com offers an API for this.

### What information do I need to provide?

Required: product. Optional: page.

### What does it return?

It returns url, page, offers, productId, total_offers, has_next_page.

### Do I need to be logged in to ebay.com?

No. It only uses pages of ebay.com that are reachable without signing in.

### Does it change anything on ebay.com, or only read data?

It only reads. It looks things up on ebay.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/ebay.com/get-product-offers, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/ebay.com/get-product-offers

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/ebay.com/get-product-offers
