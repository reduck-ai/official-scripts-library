# Crunchbase: Get Company People

Automatically get Company People on crunchbase.com. Founders, featured current employees, and board members/advisors for one company from Crunchbase, by permalink, with name, role/title, and Crunchbase profile link.

- Site: crunchbase.com
- Address: `reduck/crunchbase.com/get_company_people`
- Updated: 2026-08-03 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/crunchbase.com/get_company_people`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/crunchbase.com/get_company_people
```

## Input

- `permalink` (string, required): Crunchbase permalink slug for the company, e.g. "qonto".

## Output

- `founders` (array, required)
- `notFound` (boolean, required)
- `permalink` (string, required)
- `featuredEmployees` (array, required): A curated subset of current employees Crunchbase features on the profile - not the full headcount.
- `boardMembersAndAdvisors` (array, required)

## FAQ

### What does "Crunchbase: Get Company People" do?

Founders, featured current employees, and board members/advisors for one company from Crunchbase, by permalink, with name, role/title, and Crunchbase profile link.

### How do I automatically get Company People on crunchbase.com?

Ask an AI agent connected to Reduck to run reduck/crunchbase.com/get_company_people, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/crunchbase.com/get_company_people

### Is there a crunchbase.com API to get Company People?

You do not need one. "Crunchbase: Get Company People" drives the real crunchbase.com pages in a browser, so it works whether or not crunchbase.com offers an API for this.

### What information do I need to provide?

Required: permalink.

### What does it return?

It returns founders, notFound, permalink, featuredEmployees, boardMembersAndAdvisors.

### Do I need to be logged in to crunchbase.com?

No. It only uses pages of crunchbase.com that are reachable without signing in.

### Does it change anything on crunchbase.com, or only read data?

Unknown: its author has not declared whether it changes anything on crunchbase.com, so treat it as if it could.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/crunchbase.com/get_company_people, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/crunchbase.com/get_company_people

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/crunchbase.com/get_company_people
