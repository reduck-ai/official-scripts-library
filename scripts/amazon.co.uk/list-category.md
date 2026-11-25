# List Amazon.co.uk category page

Automatically list Amazon.co.uk category page on amazon.co.uk. List one page of an Amazon.co.uk search or category listing, from its link as shown on Amazon: the products in page order (ASIN, position, sponsored flag). Pass the ASINs to Get Amazon.co.uk product for details.

- Site: amazon.co.uk
- Address: `reduck/amazon.co.uk/list-category`
- Updated: 2026-11-24 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/amazon.co.uk/list-category`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/amazon.co.uk/list-category
```

## Input

- `url` (string, required): The results link of an Amazon.co.uk search or category, as shown on Amazon.
- `zipCode` (string, optional): UK postcode used to pin the store location.

## Output

- `url` (string, required)
- `products` (array, required)
- `heading` (string | null, optional)

## FAQ

### What does "List Amazon.co.uk category page" do?

List one page of an Amazon.co.uk search or category listing, from its link as shown on Amazon: the products in page order (ASIN, position, sponsored flag). Pass the ASINs to Get Amazon.co.uk product for details.

### How do I automatically list Amazon.co.uk category page on amazon.co.uk?

Ask an AI agent connected to Reduck to run reduck/amazon.co.uk/list-category, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/amazon.co.uk/list-category

### Is there a amazon.co.uk API to list Amazon.co.uk category page?

You do not need one. "List Amazon.co.uk category page" drives the real amazon.co.uk pages in a browser, so it works whether or not amazon.co.uk offers an API for this.

### What information do I need to provide?

Required: url. Optional: zipCode.

### What does it return?

It returns url, heading, products.

### Do I need to be logged in to amazon.co.uk?

No. It only uses pages of amazon.co.uk that are reachable without signing in.

### Does it change anything on amazon.co.uk, or only read data?

It only reads. It looks things up on amazon.co.uk and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/amazon.co.uk/list-category, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/amazon.co.uk/list-category

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/amazon.co.uk/list-category
