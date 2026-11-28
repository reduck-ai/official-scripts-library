# Add Dangdang product to cart

Automatically add Dangdang product to cart on dangdang.com. Add a product of the Dangdang Chinese store (dangdang.com) to the shopping cart of this browser, from its product id or product page link, with a quantity from 1 to 10, as the product page's add to cart button does. Returns the cart as the site holds it afterwards, in the shape List Dangdang cart items gives, plus the product id, offer id (always null: Dangdang has one seller for each product), name and units added. Works as a guest, with no account: lines already in the cart stay. A product the site does not know, a product that is sold out, and an add the site refuses fail with an error that says so. Nothing is paid or ordered. Use a managed browser in China (country CN).

- Site: dangdang.com
- Address: `reduck/dangdang.com/add_to_cart`
- Updated: 2026-11-27 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/dangdang.com/add_to_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/dangdang.com/add_to_cart
```

## Input

- `product` (string, required): Product id from Search Dangdang products (for example 29996911), or a product page link.
- `quantity` (integer, optional): How many units to add.

## Output

- `name` (string | null, required)
- `added` (integer, required): Units this run added.
- `count` (integer, required): Units in the cart.
- `lines` (array, required)
- `total` (number, required): Items total in yuan, delivery not included.
- `offerId` (string | null, required)
- `currency` (string, required)
- `productId` (string, required)

## FAQ

### What does "Add Dangdang product to cart" do?

Add a product of the Dangdang Chinese store (dangdang.com) to the shopping cart of this browser, from its product id or product page link, with a quantity from 1 to 10, as the product page's add to cart button does. Returns the cart as the site holds it afterwards, in the shape List Dangdang cart items gives, plus the product id, offer id (always null: Dangdang has one seller for each product), name and units added. Works as a guest, with no account: lines already in the cart stay. A product the site does not know, a product that is sold out, and an add the site refuses fail with an error that says so. Nothing is paid or ordered. Use a managed browser in China (country CN).

### How do I automatically add Dangdang product to cart on dangdang.com?

Ask an AI agent connected to Reduck to run reduck/dangdang.com/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/dangdang.com/add_to_cart

### Is there a dangdang.com API to add Dangdang product to cart?

You do not need one. "Add Dangdang product to cart" drives the real dangdang.com pages in a browser, so it works whether or not dangdang.com offers an API for this.

### What information do I need to provide?

Required: product. Optional: quantity.

### What does it return?

It returns name, added, count, lines, total, offerId, currency, productId.

### Do I need to be logged in to dangdang.com?

No. It only uses pages of dangdang.com that are reachable without signing in.

### Does it change anything on dangdang.com, or only read data?

It makes changes on dangdang.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/dangdang.com/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/dangdang.com/add_to_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/dangdang.com/add_to_cart
