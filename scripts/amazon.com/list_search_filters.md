# List Amazon search filters

Automatically list Amazon search filters on amazon.com. List the filters Amazon offers for a product search: the departments, the sort orders, and the refinements of its left column for this query (Prime and delivery speed, brands, customer reviews, price bands, condition, seller, deals, and the product's own attributes such as length or color). Each filter comes with the value Search Amazon products takes: department and sort as they are, refinements as group:value. Refinements depend on the query and the department, so ask for the search you will run.

- Site: amazon.com
- Address: `reduck/amazon.com/list_search_filters`
- Updated: 2026-10-16 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/amazon.com/list_search_filters`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/amazon.com/list_search_filters
```

## Input

- `query` (string, required): The search query, as you will pass it to Search Amazon products.
- `zipCode` (string, optional): US ZIP used to pin the store location.
- `department` (string, optional): Department search alias (e.g. "stripbooks"), to get that department's refinements. Default: all departments.

## Output

- `query` (string, required)
- `filters` (array, required): One row per option. key is the Search Amazon products arg it goes in (department, sort or refinements); value is what to put there.
- `department` (string | null, optional)

## FAQ

### What does "List Amazon search filters" do?

List the filters Amazon offers for a product search: the departments, the sort orders, and the refinements of its left column for this query (Prime and delivery speed, brands, customer reviews, price bands, condition, seller, deals, and the product's own attributes such as length or color). Each filter comes with the value Search Amazon products takes: department and sort as they are, refinements as group:value. Refinements depend on the query and the department, so ask for the search you will run.

### How do I automatically list Amazon search filters on amazon.com?

Ask an AI agent connected to Reduck to run reduck/amazon.com/list_search_filters, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/amazon.com/list_search_filters

### Is there a amazon.com API to list Amazon search filters?

You do not need one. "List Amazon search filters" drives the real amazon.com pages in a browser, so it works whether or not amazon.com offers an API for this.

### What information do I need to provide?

Required: query. Optional: zipCode, department.

### What does it return?

It returns query, filters, department.

### Do I need to be logged in to amazon.com?

No. It only uses pages of amazon.com that are reachable without signing in.

### Does it change anything on amazon.com, or only read data?

It only reads. It looks things up on amazon.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/amazon.com/list_search_filters, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/amazon.com/list_search_filters

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/amazon.com/list_search_filters
