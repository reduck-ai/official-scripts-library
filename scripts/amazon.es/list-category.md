# List Amazon.es category page

Automatically list Amazon.es category page on amazon.es. List one page of an Amazon.es search or category listing, from its link as shown on Amazon: the products in page order (ASIN, position, sponsored flag). Pass the ASINs to Get Amazon.es product for details.

- Site: amazon.es
- Address: `reduck/amazon.es/list-category`
- Updated: 2026-11-24 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/amazon.es/list-category`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/amazon.es/list-category
```

## Input

- `url` (string, required): The results link of an Amazon.es search or category, as shown on Amazon.
- `zipCode` (string, optional): Spanish postcode used to pin the store location.

## Output

- `url` (string, required)
- `products` (array, required)
- `heading` (string | null, optional)

## FAQ

### What does "List Amazon.es category page" do?

List one page of an Amazon.es search or category listing, from its link as shown on Amazon: the products in page order (ASIN, position, sponsored flag). Pass the ASINs to Get Amazon.es product for details.

### How do I automatically list Amazon.es category page on amazon.es?

Ask an AI agent connected to Reduck to run reduck/amazon.es/list-category, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/amazon.es/list-category

### Is there a amazon.es API to list Amazon.es category page?

You do not need one. "List Amazon.es category page" drives the real amazon.es pages in a browser, so it works whether or not amazon.es offers an API for this.

### What information do I need to provide?

Required: url. Optional: zipCode.

### What does it return?

It returns url, heading, products.

### Do I need to be logged in to amazon.es?

No. It only uses pages of amazon.es that are reachable without signing in.

### Does it change anything on amazon.es, or only read data?

It only reads. It looks things up on amazon.es and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/amazon.es/list-category, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/amazon.es/list-category

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/amazon.es/list-category
