# List Amazon.fr search filters

Automatically list Amazon.fr search filters on amazon.fr. List the filters Amazon.fr offers for a product search: the departments, the sort orders, and the refinements of its left column for this query (Prime and delivery speed, brands, customer reviews, price bands, condition, seller, deals, and the product's own attributes such as length or color). Each filter comes with the value Search Amazon products takes: department and sort as they are, refinements as group:value. Refinements depend on the query and the department, so ask for the search you will run.

- Site: amazon.fr
- Address: `reduck/amazon.fr/list_search_filters`
- Updated: 2026-10-31 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/amazon.fr/list_search_filters`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/amazon.fr/list_search_filters
```

## Input

- `query` (string, required): The search query, as you will pass it to Search Amazon products.
- `zipCode` (string, optional): French postcode used to pin the store location.
- `department` (string, optional): Department search alias (e.g. "stripbooks"), to get that department's refinements. Default: all departments.

## Output

- `query` (string, required)
- `filters` (array, required): One row per option. key is the Search Amazon products arg it goes in (department, sort or refinements); value is what to put there.
- `department` (string | null, optional)

## FAQ

### What does "List Amazon.fr search filters" do?

List the filters Amazon.fr offers for a product search: the departments, the sort orders, and the refinements of its left column for this query (Prime and delivery speed, brands, customer reviews, price bands, condition, seller, deals, and the product's own attributes such as length or color). Each filter comes with the value Search Amazon products takes: department and sort as they are, refinements as group:value. Refinements depend on the query and the department, so ask for the search you will run.

### How do I automatically list Amazon.fr search filters on amazon.fr?

Ask an AI agent connected to Reduck to run reduck/amazon.fr/list_search_filters, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/amazon.fr/list_search_filters

### Is there a amazon.fr API to list Amazon.fr search filters?

You do not need one. "List Amazon.fr search filters" drives the real amazon.fr pages in a browser, so it works whether or not amazon.fr offers an API for this.

### What information do I need to provide?

Required: query. Optional: zipCode, department.

### What does it return?

It returns query, filters, department.

### Do I need to be logged in to amazon.fr?

No. It only uses pages of amazon.fr that are reachable without signing in.

### Does it change anything on amazon.fr, or only read data?

It only reads. It looks things up on amazon.fr and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/amazon.fr/list_search_filters, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/amazon.fr/list_search_filters

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/amazon.fr/list_search_filters
