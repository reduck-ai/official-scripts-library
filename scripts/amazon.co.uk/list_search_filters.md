# List Amazon.co.uk search filters

Automatically list Amazon.co.uk search filters on amazon.co.uk. List the filters Amazon.co.uk offers for a product search: departments, sort orders and the refinements of its left column for this query. Each filter gives the value Search Amazon.co.uk products takes.

- Site: amazon.co.uk
- Address: `reduck/amazon.co.uk/list_search_filters`
- Updated: 2026-11-24 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/amazon.co.uk/list_search_filters`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/amazon.co.uk/list_search_filters
```

## Input

- `query` (string, required): The search query, as you will pass it to Search Amazon.co.uk products.
- `zipCode` (string, optional): UK postcode used to pin the store location.
- `department` (string, optional): Department search alias, to get that department's refinements.

## Output

- `query` (string, required)
- `filters` (array, required)
- `department` (string | null, optional)

## FAQ

### What does "List Amazon.co.uk search filters" do?

List the filters Amazon.co.uk offers for a product search: departments, sort orders and the refinements of its left column for this query. Each filter gives the value Search Amazon.co.uk products takes.

### How do I automatically list Amazon.co.uk search filters on amazon.co.uk?

Ask an AI agent connected to Reduck to run reduck/amazon.co.uk/list_search_filters, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/amazon.co.uk/list_search_filters

### Is there a amazon.co.uk API to list Amazon.co.uk search filters?

You do not need one. "List Amazon.co.uk search filters" drives the real amazon.co.uk pages in a browser, so it works whether or not amazon.co.uk offers an API for this.

### What information do I need to provide?

Required: query. Optional: zipCode, department.

### What does it return?

It returns query, filters, department.

### Do I need to be logged in to amazon.co.uk?

No. It only uses pages of amazon.co.uk that are reachable without signing in.

### Does it change anything on amazon.co.uk, or only read data?

It only reads. It looks things up on amazon.co.uk and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/amazon.co.uk/list_search_filters, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/amazon.co.uk/list_search_filters

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/amazon.co.uk/list_search_filters
