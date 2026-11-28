# Get Dangdang product

Automatically get Dangdang product on dangdang.com. Read one product of the Dangdang Chinese store (dangdang.com) from its product id or its product page link: name, subtitle, link, seller (Dangdang itself or a marketplace shop, with its shop id), selling price and list price in yuan, whether it is in stock, review count, categories, the key facts the page lists (for a book the author, publisher and book number), and images. Stock and price are what a new guest sees online with no delivery address chosen. A product id or link that the site does not know fails with an error that says so. Dangdang has one seller for each product, so there is no offers script. Use a managed browser in China (country CN): other places can get a slide verification.

- Site: dangdang.com
- Address: `reduck/dangdang.com/get-product`
- Updated: 2026-11-27 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/dangdang.com/get-product`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/dangdang.com/get-product
```

## Input

- `product` (string, required): Product id from Search Dangdang products (for example 29996911), or a product page link.

## Output

- `url` (string, required)
- `name` (string, required)
- `price` (number | null, required): Selling price in yuan.
- `images` (array, required)
- `seller` (string, required): Shop name as the site writes it, in Chinese. 当当网 is Dangdang itself.
- `shopId` (string | null, required): Id of the marketplace shop; null when Dangdang sells it.
- `currency` (string, required)
- `subtitle` (string | null, required)
- `listPrice` (number | null, required): List price in yuan, as the page shows it.
- `productId` (string, required)
- `attributes` (array, required)
- `categories` (array, required): The page's category path, from the widest category to the narrowest.
- `sellerType` (string, required): self when Dangdang sells it, marketplace when a shop does.
- `reviewCount` (integer | null, required)
- `availability` (string, required): InStock when the page offers add to cart, OutOfStock when it shows the sold out button, Unknown otherwise.

## FAQ

### What does "Get Dangdang product" do?

Read one product of the Dangdang Chinese store (dangdang.com) from its product id or its product page link: name, subtitle, link, seller (Dangdang itself or a marketplace shop, with its shop id), selling price and list price in yuan, whether it is in stock, review count, categories, the key facts the page lists (for a book the author, publisher and book number), and images. Stock and price are what a new guest sees online with no delivery address chosen. A product id or link that the site does not know fails with an error that says so. Dangdang has one seller for each product, so there is no offers script. Use a managed browser in China (country CN): other places can get a slide verification.

### How do I automatically get Dangdang product on dangdang.com?

Ask an AI agent connected to Reduck to run reduck/dangdang.com/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/dangdang.com/get-product

### Is there a dangdang.com API to get Dangdang product?

You do not need one. "Get Dangdang product" drives the real dangdang.com pages in a browser, so it works whether or not dangdang.com offers an API for this.

### What information do I need to provide?

Required: product.

### What does it return?

It returns url, name, price, images, seller, shopId, currency, subtitle, listPrice, productId, attributes, categories, sellerType, reviewCount, availability.

### Do I need to be logged in to dangdang.com?

No. It only uses pages of dangdang.com that are reachable without signing in.

### Does it change anything on dangdang.com, or only read data?

It only reads. It looks things up on dangdang.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/dangdang.com/get-product, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/dangdang.com/get-product

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/dangdang.com/get-product
