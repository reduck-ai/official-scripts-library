# Get the sellers of a Flipkart product

Automatically get the sellers of a Flipkart product on flipkart.com. List every seller that sells one Flipkart India (flipkart.com) product, as its "All sellers" page shows them, by product id (the product_id of Search Flipkart products) or product link. For each offer: the offer id (pass it to Add a product to the Flipkart cart), seller name and id, new seller flag, price and maximum retail price in Indian rupees (INR), whether it is the offer Flipkart picks by default, cash on delivery, free delivery, Flipkart Assured and the delivery message. Also gives the product name, brand, number of sellers and lowest price. Prices and delivery are those a visitor with no delivery pincode sees. An unknown product id fails with an error that says so.

- Site: flipkart.com
- Address: `reduck/flipkart.com/get-product-offers`
- Updated: 2026-11-26 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/flipkart.com/get-product-offers`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/flipkart.com/get-product-offers
```

## Input

- `url` (string, optional): Flipkart product link with pid= in it. Used when no product_id is given.
- `product_id` (string, optional): Flipkart product id (16 letters and digits), the product_id of Search Flipkart products.

## Output

- `name` (string | null, required)
- `brand` (string | null, required)
- `offers` (array, required)
- `currency` (string, required): Always INR.
- `min_price` (number | null, required): Lowest price among the sellers, in rupees.
- `product_id` (string, required)
- `seller_count` (integer | null, required)

## FAQ

### What does "Get the sellers of a Flipkart product" do?

List every seller that sells one Flipkart India (flipkart.com) product, as its "All sellers" page shows them, by product id (the product_id of Search Flipkart products) or product link. For each offer: the offer id (pass it to Add a product to the Flipkart cart), seller name and id, new seller flag, price and maximum retail price in Indian rupees (INR), whether it is the offer Flipkart picks by default, cash on delivery, free delivery, Flipkart Assured and the delivery message. Also gives the product name, brand, number of sellers and lowest price. Prices and delivery are those a visitor with no delivery pincode sees. An unknown product id fails with an error that says so.

### How do I automatically get the sellers of a Flipkart product on flipkart.com?

Ask an AI agent connected to Reduck to run reduck/flipkart.com/get-product-offers, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/flipkart.com/get-product-offers

### Is there a flipkart.com API to get the sellers of a Flipkart product?

You do not need one. "Get the sellers of a Flipkart product" drives the real flipkart.com pages in a browser, so it works whether or not flipkart.com offers an API for this.

### What information do I need to provide?

Optional: url, product_id.

### What does it return?

It returns name, brand, offers, currency, min_price, product_id, seller_count.

### Do I need to be logged in to flipkart.com?

No. It only uses pages of flipkart.com that are reachable without signing in.

### Does it change anything on flipkart.com, or only read data?

It only reads. It looks things up on flipkart.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/flipkart.com/get-product-offers, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/flipkart.com/get-product-offers

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/flipkart.com/get-product-offers
