# Update a Jira issue

Automatically update a Jira issue on atlassian.net. Change an existing Jira Cloud issue by key: its summary, its plain-text description (replaced as a whole), its labels (replaced as a whole) and its status. The status moves through the issue's workflow, by the target status name or id; a status the workflow does not allow from where the issue is now is refused with the ones it allows. Fields left out are not touched. The issue is read back from Jira afterwards and returned.

- Site: atlassian.net
- Address: `reduck/atlassian.net/update_issue`
- Updated: 2026-11-04 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/atlassian.net/update_issue`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/atlassian.net/update_issue
```

## Input

- `key` (string, required): The issue key: the project key, a dash and the number, as list_issues or create_issue return it.
- `site` (string, required): The Jira Cloud site, e.g. acme.atlassian.net (or just acme).
- `labels` (array, optional): The full new set of labels; an empty list removes them all.
- `status` (string, optional): The status to move the issue to, by its name as the site shows it or its id.
- `summary` (string, optional)
- `description` (string, optional): New plain-text description; each line becomes a paragraph. An empty string clears it.

## Output

- `id` (string, required)
- `key` (string, required)
- `url` (string, required)
- `changed` (array, required): The fields this run changed: summary, description, labels, status.
- `summary` (string, required)
- `labels` (array, optional)
- `status` (string | null, optional)
- `created` (string | null, optional)
- `project` (string | null, optional)
- `updated` (string | null, optional)
- `assignee` (string | null, optional)
- `priority` (string | null, optional)
- `reporter` (string | null, optional)
- `issueType` (string | null, optional)
- `description` (string | null, optional)
- `statusCategory` (string | null, optional)

## FAQ

### What does "Update a Jira issue" do?

Change an existing Jira Cloud issue by key: its summary, its plain-text description (replaced as a whole), its labels (replaced as a whole) and its status. The status moves through the issue's workflow, by the target status name or id; a status the workflow does not allow from where the issue is now is refused with the ones it allows. Fields left out are not touched. The issue is read back from Jira afterwards and returned.

### How do I automatically update a Jira issue on atlassian.net?

Ask an AI agent connected to Reduck to run reduck/atlassian.net/update_issue, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/atlassian.net/update_issue

### Is there a atlassian.net API to update a Jira issue?

You do not need one. "Update a Jira issue" drives the real atlassian.net pages in a browser, so it works whether or not atlassian.net offers an API for this.

### What information do I need to provide?

Required: site, key. Optional: labels, status, summary, description.

### What does it return?

It returns id, key, url, labels, status, changed, created, project, summary, updated, assignee, priority, reporter, issueType, description, statusCategory.

### Do I need to be logged in to atlassian.net?

Yes. It acts as you on atlassian.net: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the atlassian.net cookies saved by the Reduck extension.

### Does it change anything on atlassian.net, or only read data?

It makes changes on atlassian.net, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/atlassian.net/update_issue, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/atlassian.net/update_issue

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/atlassian.net/update_issue
