# List Amazon.es search filters

Automatically list Amazon.es search filters on amazon.es. List the filters Amazon.es offers for a product search: departments, sort orders and the refinements of its left column for this query. Each filter gives the value Search Amazon.es products takes.

- Site: amazon.es
- Address: `reduck/amazon.es/list_search_filters`
- Updated: 2026-11-24 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/amazon.es/list_search_filters`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/amazon.es/list_search_filters
```

## Input

- `query` (string, required): The search query, as you will pass it to Search Amazon.es products.
- `zipCode` (string, optional): Spanish postcode used to pin the store location.
- `department` (string, optional): Department search alias, to get that department's refinements.

## Output

- `query` (string, required)
- `filters` (array, required)
- `department` (string | null, optional)

## FAQ

### What does "List Amazon.es search filters" do?

List the filters Amazon.es offers for a product search: departments, sort orders and the refinements of its left column for this query. Each filter gives the value Search Amazon.es products takes.

### How do I automatically list Amazon.es search filters on amazon.es?

Ask an AI agent connected to Reduck to run reduck/amazon.es/list_search_filters, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/amazon.es/list_search_filters

### Is there a amazon.es API to list Amazon.es search filters?

You do not need one. "List Amazon.es search filters" drives the real amazon.es pages in a browser, so it works whether or not amazon.es offers an API for this.

### What information do I need to provide?

Required: query. Optional: zipCode, department.

### What does it return?

It returns query, filters, department.

### Do I need to be logged in to amazon.es?

No. It only uses pages of amazon.es that are reachable without signing in.

### Does it change anything on amazon.es, or only read data?

It only reads. It looks things up on amazon.es and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/amazon.es/list_search_filters, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/amazon.es/list_search_filters

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/amazon.es/list_search_filters
