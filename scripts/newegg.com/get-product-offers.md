# Get Newegg product offers

Automatically get Newegg product offers on newegg.com. List every seller's offer for one Newegg (newegg.com) product, from its item number or link: offer item number, seller, price after instant rebate, list price, shipping cost, ships-from country and stock. A link that is not a product page, or an unknown item, is refused with a clear message.

- Site: newegg.com
- Address: `reduck/newegg.com/get-product-offers`
- Updated: 2026-11-25 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/newegg.com/get-product-offers`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/newegg.com/get-product-offers
```

## Input

- `item` (string, required): Newegg item number (e.g. N82E16820242902, 20-242-902, 9SIA...) or a newegg.com/p/<item> product link.

## Output

- `name` (string | null, required)
- `count` (integer, required)
- `offers` (array, required)
- `productId` (string, required)

## FAQ

### What does "Get Newegg product offers" do?

List every seller's offer for one Newegg (newegg.com) product, from its item number or link: offer item number, seller, price after instant rebate, list price, shipping cost, ships-from country and stock. A link that is not a product page, or an unknown item, is refused with a clear message.

### How do I automatically get Newegg product offers on newegg.com?

Ask an AI agent connected to Reduck to run reduck/newegg.com/get-product-offers, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/newegg.com/get-product-offers

### Is there a newegg.com API to get Newegg product offers?

You do not need one. "Get Newegg product offers" drives the real newegg.com pages in a browser, so it works whether or not newegg.com offers an API for this.

### What information do I need to provide?

Required: item.

### What does it return?

It returns name, count, offers, productId.

### Do I need to be logged in to newegg.com?

No. It only uses pages of newegg.com that are reachable without signing in.

### Does it change anything on newegg.com, or only read data?

It only reads. It looks things up on newegg.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/newegg.com/get-product-offers, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/newegg.com/get-product-offers

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/newegg.com/get-product-offers
