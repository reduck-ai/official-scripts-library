# Add a product to the Rue du Commerce cart

Automatically add a product to the Rue du Commerce cart on rueducommerce.fr. Adds a product to the guest cart of rueducommerce.fr from its product link, product id or offer id, with a quantity from 1 to 10, and returns the cart after the addition. No order is placed. A link that is not a product page, or a product the site cannot add, is refused with a clear message.

- Site: rueducommerce.fr
- Address: `reduck/rueducommerce.fr/add_to_cart`
- Updated: 2026-11-24 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/rueducommerce.fr/add_to_cart`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/rueducommerce.fr/add_to_cart
```

## Input

- `product` (string, required): A www.rueducommerce.fr/p/<id>.html link, a product id (for example r25109147605), or an offer id (for example AR202509260012) from search-products or get-product.
- `quantity` (integer, optional): Number of units to add.
- `isMarketplace` (boolean, optional): Only with an offer id: true when the offer comes from a marketplace seller, as search-products reports. A link or product id finds it by itself.

## Output

- `added` (integer, required)
- `count` (integer, required)
- `lines` (array, required)
- `total` (number | null, required)
- `offerId` (string, required)
- `name` (string | null, optional)
- `productId` (string | null, optional)

## FAQ

### What does "Add a product to the Rue du Commerce cart" do?

Adds a product to the guest cart of rueducommerce.fr from its product link, product id or offer id, with a quantity from 1 to 10, and returns the cart after the addition. No order is placed. A link that is not a product page, or a product the site cannot add, is refused with a clear message.

### How do I automatically add a product to the Rue du Commerce cart on rueducommerce.fr?

Ask an AI agent connected to Reduck to run reduck/rueducommerce.fr/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/rueducommerce.fr/add_to_cart

### Is there a rueducommerce.fr API to add a product to the Rue du Commerce cart?

You do not need one. "Add a product to the Rue du Commerce cart" drives the real rueducommerce.fr pages in a browser, so it works whether or not rueducommerce.fr offers an API for this.

### What information do I need to provide?

Required: product. Optional: quantity, isMarketplace.

### What does it return?

It returns name, added, count, lines, total, offerId, productId.

### Do I need to be logged in to rueducommerce.fr?

No. It only uses pages of rueducommerce.fr that are reachable without signing in.

### Does it change anything on rueducommerce.fr, or only read data?

It makes changes on rueducommerce.fr, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/rueducommerce.fr/add_to_cart, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/rueducommerce.fr/add_to_cart

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/rueducommerce.fr/add_to_cart
