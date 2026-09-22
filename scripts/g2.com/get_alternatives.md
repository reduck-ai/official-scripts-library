# Get G2 product alternatives

Automatically get G2 product alternatives on g2.com. List a G2 product's alternatives/competitors from its Alternatives page: name, product slug, and G2 rating. No login required.

- Site: g2.com
- Address: `reduck/g2.com/get_alternatives`
- Updated: 2026-09-02 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/g2.com/get_alternatives`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/g2.com/get_alternatives
```

## Input

- `product_slug` (string, required): G2 product URL slug, e.g. "slack" (from g2.com/products/<slug>/competitors/alternatives)

## Output

- `alternatives` (array, required)
- `product_slug` (string, required)

## FAQ

### What does "Get G2 product alternatives" do?

List a G2 product's alternatives/competitors from its Alternatives page: name, product slug, and G2 rating. No login required.

### How do I automatically get G2 product alternatives on g2.com?

Ask an AI agent connected to Reduck to run reduck/g2.com/get_alternatives, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/g2.com/get_alternatives

### Is there a g2.com API to get G2 product alternatives?

You do not need one. "Get G2 product alternatives" drives the real g2.com pages in a browser, so it works whether or not g2.com offers an API for this.

### What information do I need to provide?

Required: product_slug.

### What does it return?

It returns alternatives, product_slug.

### Do I need to be logged in to g2.com?

No. It only uses pages of g2.com that are reachable without signing in.

### Does it change anything on g2.com, or only read data?

It only reads. It looks things up on g2.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/g2.com/get_alternatives, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/g2.com/get_alternatives

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/g2.com/get_alternatives
