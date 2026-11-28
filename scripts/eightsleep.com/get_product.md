# Get Eight Sleep product and its offers

Automatically get Eight Sleep product and its offers on eightsleep.com. Read one Eight Sleep US product page: name, description, category, photos, star rating and review count, and every offer the store sells for it (size, zone or pack option) with its offer id, SKU, price, price before discount, discount codes and stock state, in US dollars. Pass the offer id to eightsleep.com/add_to_cart. Get product ids from eightsleep.com/list_products; the Pod is pod-cover. A product id with no page gives an error that says so.

- Site: eightsleep.com
- Address: `reduck/eightsleep.com/get_product`
- Updated: 2026-11-27 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/eightsleep.com/get_product`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/eightsleep.com/get_product
```

## Input

- `product` (string, required): The product's page id, e.g. pillow or pod-cover, or its page link, e.g. https://www.eightsleep.com/product/pillow/.

## Output

- `url` (string, required)
- `offers` (array, required)
- `productId` (string, required): The store's product id, the productId of the cart lines.
- `name` (string | null, optional)
- `images` (array, optional)
- `rating` (number | null, optional)
- `category` (string | null, optional)
- `currency` (string | null, optional)
- `catalogId` (string | null, optional)
- `description` (string | null, optional)
- `reviewCount` (integer | null, optional)

## FAQ

### What does "Get Eight Sleep product and its offers" do?

Read one Eight Sleep US product page: name, description, category, photos, star rating and review count, and every offer the store sells for it (size, zone or pack option) with its offer id, SKU, price, price before discount, discount codes and stock state, in US dollars. Pass the offer id to eightsleep.com/add_to_cart. Get product ids from eightsleep.com/list_products; the Pod is pod-cover. A product id with no page gives an error that says so.

### How do I automatically get Eight Sleep product and its offers on eightsleep.com?

Ask an AI agent connected to Reduck to run reduck/eightsleep.com/get_product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/eightsleep.com/get_product

### Is there a eightsleep.com API to get Eight Sleep product and its offers?

You do not need one. "Get Eight Sleep product and its offers" drives the real eightsleep.com pages in a browser, so it works whether or not eightsleep.com offers an API for this.

### What information do I need to provide?

Required: product.

### What does it return?

It returns url, name, images, offers, rating, category, currency, catalogId, productId, description, reviewCount.

### Do I need to be logged in to eightsleep.com?

No. It only uses pages of eightsleep.com that are reachable without signing in.

### Does it change anything on eightsleep.com, or only read data?

It only reads. It looks things up on eightsleep.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/eightsleep.com/get_product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/eightsleep.com/get_product

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/eightsleep.com/get_product
