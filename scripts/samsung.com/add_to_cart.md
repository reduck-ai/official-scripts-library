# Add a product to the Samsung cart

Automatically add a product to the Samsung cart on samsung.com. Add a product of the Samsung US store (samsung.com/us) to the cart of this browser, by its model code (SKU) or its product link, with a quantity from 1 to 10, and return the whole cart afterwards: each line with its line id, product id (the model code), offer id, name, seller (always Samsung), quantity, unit price and line price in US dollars, plus the item count and the subtotal, and the product added with the number of units Samsung added. Pick the configuration (color, storage, size, carrier) with Get Samsung product: each one has its own model code. Works as a guest, with no account; lines already in the cart stay. Nothing is paid or ordered. A family page link with no model code, an unknown model code, and a product or quantity Samsung does not sell online fail with an error that gives Samsung's reason.

- Site: samsung.com
- Address: `reduck/samsung.com/add_to_cart`
- Updated: 2026-11-26 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/samsung.com/add_to_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/samsung.com/add_to_cart
```

## Input

- `url` (string, optional): Samsung US product link that ends with the model code. Used when no product_id is given.
- `quantity` (integer, optional): Number of units to add, 1 to 10.
- `product_id` (string, optional): Samsung model code (SKU) of the exact configuration, as productId of Get Samsung product or Search Samsung products.

## Output

- `name` (string | null, required)
- `added` (integer, required): Units Samsung added by this call.
- `count` (integer, required): Number of units in the cart after the add, all lines together.
- `lines` (array, required)
- `total` (number | null, required): Subtotal of the cart in US dollars, before tax and delivery.
- `offerId` (string | null, required): The same model code: Samsung sells each configuration under one code.
- `productId` (string, required): Model code of the product added.

## FAQ

### What does "Add a product to the Samsung cart" do?

Add a product of the Samsung US store (samsung.com/us) to the cart of this browser, by its model code (SKU) or its product link, with a quantity from 1 to 10, and return the whole cart afterwards: each line with its line id, product id (the model code), offer id, name, seller (always Samsung), quantity, unit price and line price in US dollars, plus the item count and the subtotal, and the product added with the number of units Samsung added. Pick the configuration (color, storage, size, carrier) with Get Samsung product: each one has its own model code. Works as a guest, with no account; lines already in the cart stay. Nothing is paid or ordered. A family page link with no model code, an unknown model code, and a product or quantity Samsung does not sell online fail with an error that gives Samsung's reason.

### How do I automatically add a product to the Samsung cart on samsung.com?

Ask an AI agent connected to Reduck to run reduck/samsung.com/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/samsung.com/add_to_cart

### Is there a samsung.com API to add a product to the Samsung cart?

You do not need one. "Add a product to the Samsung cart" drives the real samsung.com pages in a browser, so it works whether or not samsung.com offers an API for this.

### What information do I need to provide?

Optional: url, quantity, product_id.

### What does it return?

It returns name, added, count, lines, total, offerId, productId.

### Do I need to be logged in to samsung.com?

No. It only uses pages of samsung.com that are reachable without signing in.

### Does it change anything on samsung.com, or only read data?

It makes changes on samsung.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/samsung.com/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/samsung.com/add_to_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/samsung.com/add_to_cart
