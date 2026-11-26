# Get Home Depot product

Automatically get Home Depot product on homedepot.com. Reads one homedepot.com product from its itemId (Internet number) or product link: name, brand, model, price, rating, description, images, availability and the per-order quantity limit. An unknown id or a link that is not a product page is refused with a clear message.

- Site: homedepot.com
- Address: `reduck/homedepot.com/get-product`
- Updated: 2026-11-25 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/homedepot.com/get-product`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/homedepot.com/get-product
```

## Input

- `product` (string, required): The itemId (e.g. "342705642") or a product link from Search Home Depot products.

## Output

- `itemId` (string, required)
- `upc` (string | null, optional)
- `url` (string | null, optional)
- `name` (string | null, optional)
- `brand` (string | null, optional)
- `image` (string | null, optional)
- `price` (number | null, optional)
- `images` (array, optional)
- `rating` (number | null, optional)
- `buyable` (boolean | null, optional)
- `returnable` (string | null, optional)
- `description` (string | null, optional)
- `modelNumber` (string | null, optional)
- `reviewCount` (number | null, optional)
- `discontinued` (boolean | null, optional)
- `originalPrice` (number | null, optional)
- `quantityLimit` (number | null, optional)
- `storeSkuNumber` (string | null, optional)
- `availabilityType` (string | null, optional)

## FAQ

### What does "Get Home Depot product" do?

Reads one homedepot.com product from its itemId (Internet number) or product link: name, brand, model, price, rating, description, images, availability and the per-order quantity limit. An unknown id or a link that is not a product page is refused with a clear message.

### How do I automatically get Home Depot product on homedepot.com?

Ask an AI agent connected to Reduck to run reduck/homedepot.com/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/homedepot.com/get-product

### Is there a homedepot.com API to get Home Depot product?

You do not need one. "Get Home Depot product" drives the real homedepot.com pages in a browser, so it works whether or not homedepot.com offers an API for this.

### What information do I need to provide?

Required: product.

### What does it return?

It returns upc, url, name, brand, image, price, images, itemId, rating, buyable, returnable, description, modelNumber, reviewCount, discontinued, originalPrice, quantityLimit, storeSkuNumber, availabilityType.

### Do I need to be logged in to homedepot.com?

No. It only uses pages of homedepot.com that are reachable without signing in.

### Does it change anything on homedepot.com, or only read data?

It only reads. It looks things up on homedepot.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/homedepot.com/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/homedepot.com/get-product

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/homedepot.com/get-product
