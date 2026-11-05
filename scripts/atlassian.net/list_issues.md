# List Jira issues

Automatically list Jira issues on atlassian.net. List the issues on a Jira Cloud site, for one project or any JQL query, newest first by default: key, summary, description, status, type, priority, assignee, reporter, labels and dates. Jira refuses a query with no restriction, so pass a project key, a JQL query, or both. Pages through results with nextPageToken; an empty list means nothing matched.

- Site: atlassian.net
- Address: `reduck/atlassian.net/list_issues`
- Updated: 2026-11-04 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/atlassian.net/list_issues`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/atlassian.net/list_issues
```

## Input

- `site` (string, required): The Jira Cloud site, e.g. acme.atlassian.net (or just acme).
- `jql` (string, optional): A JQL query, e.g. status = "In Progress" order by updated desc. When it has no order by clause, results are newest first.
- `project` (string, optional): A project key, the prefix of its issue keys. Combined with jql when both are given.
- `maxResults` (integer, optional): Issues per page.
- `nextPageToken` (string, optional): The nextPageToken of the previous page, to read the next one.

## Output

- `jql` (string, required): The query Jira ran.
- `site` (string, required)
- `isLast` (boolean, required)
- `issues` (array, required)
- `nextPageToken` (string | null, optional)

## FAQ

### What does "List Jira issues" do?

List the issues on a Jira Cloud site, for one project or any JQL query, newest first by default: key, summary, description, status, type, priority, assignee, reporter, labels and dates. Jira refuses a query with no restriction, so pass a project key, a JQL query, or both. Pages through results with nextPageToken; an empty list means nothing matched.

### How do I automatically list Jira issues on atlassian.net?

Ask an AI agent connected to Reduck to run reduck/atlassian.net/list_issues, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/atlassian.net/list_issues

### Is there a atlassian.net API to list Jira issues?

You do not need one. "List Jira issues" drives the real atlassian.net pages in a browser, so it works whether or not atlassian.net offers an API for this.

### What information do I need to provide?

Required: site. Optional: jql, project, maxResults, nextPageToken.

### What does it return?

It returns jql, site, isLast, issues, nextPageToken.

### Do I need to be logged in to atlassian.net?

Yes. It acts as you on atlassian.net: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the atlassian.net cookies saved by the Reduck extension.

### Does it change anything on atlassian.net, or only read data?

It only reads. It looks things up on atlassian.net and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/atlassian.net/list_issues, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/atlassian.net/list_issues

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/atlassian.net/list_issues
