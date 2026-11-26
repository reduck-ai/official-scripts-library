# Add a Dell product to the cart

Automatically add a Dell product to the cart on dell.com. Add a product of the Dell US store to the cart, by its id or link, and return the cart.

- Site: dell.com
- Address: `reduck/dell.com/add_to_cart`
- Updated: 2026-11-25 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/dell.com/add_to_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/dell.com/add_to_cart
```

## Input

- `product` (string, required): Product id as get-product or search-products returns it (e.g. "se2426h", "dx13260_so_42"), or the link of a Dell US product page. Each configuration of a computer has its own id.
- `quantity` (integer, optional): Number of units to add.

## Output

- `name` (string | null, required)
- `added` (boolean, required)
- `count` (integer, required)
- `lines` (array, required)
- `total` (number | null, required): Item subtotal after discounts, in USD, without tax and shipping.
- `offerId` (string | null, required)
- `productId` (string | null, required)

## FAQ

### What does "Add a Dell product to the cart" do?

Add a product of the Dell US store to the cart, by its id or link, and return the cart.

### How do I automatically add a Dell product to the cart on dell.com?

Ask an AI agent connected to Reduck to run reduck/dell.com/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/dell.com/add_to_cart

### Is there a dell.com API to add a Dell product to the cart?

You do not need one. "Add a Dell product to the cart" drives the real dell.com pages in a browser, so it works whether or not dell.com offers an API for this.

### What information do I need to provide?

Required: product. Optional: quantity.

### What does it return?

It returns name, added, count, lines, total, offerId, productId.

### Do I need to be logged in to dell.com?

No. It only uses pages of dell.com that are reachable without signing in.

### Does it change anything on dell.com, or only read data?

It makes changes on dell.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/dell.com/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/dell.com/add_to_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/dell.com/add_to_cart
