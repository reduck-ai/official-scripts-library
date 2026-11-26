# Get Fnac product offers

Automatically get Fnac product offers on fnac.com. List every offer for one fnac.com product, 10 sellers a page: price, condition, seller name and id, ships from, shipping price and delivery date. Fnac's own offer comes first on page 1.

- Site: fnac.com
- Address: `reduck/fnac.com/get-product-offers`
- Updated: 2026-11-25 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/fnac.com/get-product-offers`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/fnac.com/get-product-offers
```

## Input

- `product` (string, required): Fnac product id as Search Fnac products returns it (a<number> or mp<number>), or a www.fnac.com product page link.
- `page` (integer, optional): Page of the seller offers list, 10 offers a page. hasNextPage and totalPages say when to stop.

## Output

- `name` (string | null, required)
- `page` (integer, required)
- `offers` (array, required): The offers of this page, in Fnac's order. On page 1, Fnac's own offer comes first when Fnac sells the product. A page past the last one gives an empty list.
- `productId` (string, required)
- `totalPages` (integer | null, required): Pages of the seller offers list. Null on a page past the last one.
- `hasNextPage` (boolean, required)

## FAQ

### What does "Get Fnac product offers" do?

List every offer for one fnac.com product, 10 sellers a page: price, condition, seller name and id, ships from, shipping price and delivery date. Fnac's own offer comes first on page 1.

### How do I automatically get Fnac product offers on fnac.com?

Ask an AI agent connected to Reduck to run reduck/fnac.com/get-product-offers, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/fnac.com/get-product-offers

### Is there a fnac.com API to get Fnac product offers?

You do not need one. "Get Fnac product offers" drives the real fnac.com pages in a browser, so it works whether or not fnac.com offers an API for this.

### What information do I need to provide?

Required: product. Optional: page.

### What does it return?

It returns name, page, offers, productId, totalPages, hasNextPage.

### Do I need to be logged in to fnac.com?

No. It only uses pages of fnac.com that are reachable without signing in.

### Does it change anything on fnac.com, or only read data?

It only reads. It looks things up on fnac.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/fnac.com/get-product-offers, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/fnac.com/get-product-offers

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/fnac.com/get-product-offers
