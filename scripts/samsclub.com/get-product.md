# Get a Sam's Club product

Automatically get a Sam's Club product on samsclub.com. Get one Sam's Club (samsclub.com, US) product by its item id or its product link: item id, offer id, name, brand, link, price, previous price, unit price, availability, seller, rating, review count, images, description, category path, the quantity limits of one order, whether it can be added to the cart, and its options (size, color) with every combination and its own item id, to pass to Add a product to the Sam's Club cart. Prices and availability are for the club and address Sam's Club gives to the browser. An item id that Sam's Club does not know, or a link that is not a Sam's Club product page, fails with an error that says so. No account is needed.

- Site: samsclub.com
- Address: `reduck/samsclub.com/get-product`
- Updated: 2026-11-26 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/samsclub.com/get-product`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/samsclub.com/get-product
```

## Input

- `url` (string, optional): Sam's Club product link (https://www.samsclub.com/ip/<name>/<item id>). Used when no item_id is given.
- `item_id` (string, optional): Sam's Club item id (productId of Search Sam's Club products).

## Output

- `url` (string, required)
- `name` (string, required)
- `price` (number | null, required): Price in US dollars.
- `offerId` (string | null, required)
- `options` (array, required): Option names (for example Actual Color, Clothing Size) and their values; empty for a product with no options.
- `variants` (array, required): Every option combination, each with its own item id; empty for a product with no options.
- `productId` (string, required): Item id of the product the page shows; pass it to Add a product to the Sam's Club cart.
- `availability` (string | null, required): Availability as Sam's Club gives it, for example IN_STOCK or OUT_OF_STOCK.
- `canAddToCart` (boolean, required): True when the page offers an add to cart button for this item.
- `brand` (string | null, optional)
- `images` (array, optional)
- `rating` (number | null, optional)
- `seller` (string | null, optional): Sam's Club, or the marketplace seller.
- `category` (array, optional): Category path as Sam's Club gives it, from the top (it starts with All Departments).
- `wasPrice` (number | null, optional)
- `unitPrice` (string | null, optional): Unit price as the page shows it.
- `description` (string | null, optional): Short description as plain text.
- `maxQuantity` (integer | null, optional): Largest quantity of one order.
- `minQuantity` (integer | null, optional): Smallest quantity of one order.
- `reviewCount` (integer | null, optional)

## FAQ

### What does "Get a Sam's Club product" do?

Get one Sam's Club (samsclub.com, US) product by its item id or its product link: item id, offer id, name, brand, link, price, previous price, unit price, availability, seller, rating, review count, images, description, category path, the quantity limits of one order, whether it can be added to the cart, and its options (size, color) with every combination and its own item id, to pass to Add a product to the Sam's Club cart. Prices and availability are for the club and address Sam's Club gives to the browser. An item id that Sam's Club does not know, or a link that is not a Sam's Club product page, fails with an error that says so. No account is needed.

### How do I automatically get a Sam's Club product on samsclub.com?

Ask an AI agent connected to Reduck to run reduck/samsclub.com/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/samsclub.com/get-product

### Is there a samsclub.com API to get a Sam's Club product?

You do not need one. "Get a Sam's Club product" drives the real samsclub.com pages in a browser, so it works whether or not samsclub.com offers an API for this.

### What information do I need to provide?

Optional: url, item_id.

### What does it return?

It returns url, name, brand, price, images, rating, seller, offerId, options, category, variants, wasPrice, productId, unitPrice, description, maxQuantity, minQuantity, reviewCount, availability, canAddToCart.

### Do I need to be logged in to samsclub.com?

No. It only uses pages of samsclub.com that are reachable without signing in.

### Does it change anything on samsclub.com, or only read data?

It only reads. It looks things up on samsclub.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/samsclub.com/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/samsclub.com/get-product

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/samsclub.com/get-product
