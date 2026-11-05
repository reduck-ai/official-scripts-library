# Create a Jira issue

Automatically create a Jira issue on atlassian.net. Create an issue in a Jira Cloud project with a summary, and optionally a plain-text description (one paragraph per line), an issue type and labels. The issue type is matched by its name or id among the types the project offers; an unknown type is refused with the list of valid ones. The new issue is read back from Jira and returned with its key and link.

- Site: atlassian.net
- Address: `reduck/atlassian.net/create_issue`
- Updated: 2026-11-04 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/atlassian.net/create_issue`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/atlassian.net/create_issue
```

## Input

- `site` (string, required): The Jira Cloud site, e.g. acme.atlassian.net (or just acme).
- `project` (string, required): The project key, the prefix of its issue keys (list_issues returns it as project).
- `summary` (string, required): The issue title.
- `labels` (array, optional): Labels, without spaces.
- `issueType` (string, optional): An issue type name or id the project offers, e.g. Task, Story, Bug, Epic.
- `description` (string, optional): Plain text; each line becomes a paragraph.

## Output

- `id` (string, required)
- `key` (string, required)
- `url` (string, required)
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

### What does "Create a Jira issue" do?

Create an issue in a Jira Cloud project with a summary, and optionally a plain-text description (one paragraph per line), an issue type and labels. The issue type is matched by its name or id among the types the project offers; an unknown type is refused with the list of valid ones. The new issue is read back from Jira and returned with its key and link.

### How do I automatically create a Jira issue on atlassian.net?

Ask an AI agent connected to Reduck to run reduck/atlassian.net/create_issue, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/atlassian.net/create_issue

### Is there a atlassian.net API to create a Jira issue?

You do not need one. "Create a Jira issue" drives the real atlassian.net pages in a browser, so it works whether or not atlassian.net offers an API for this.

### What information do I need to provide?

Required: site, project, summary. Optional: labels, issueType, description.

### What does it return?

It returns id, key, url, labels, status, created, project, summary, updated, assignee, priority, reporter, issueType, description, statusCategory.

### Do I need to be logged in to atlassian.net?

Yes. It acts as you on atlassian.net: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the atlassian.net cookies saved by the Reduck extension.

### Does it change anything on atlassian.net, or only read data?

It makes changes on atlassian.net, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/atlassian.net/create_issue, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/atlassian.net/create_issue

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/atlassian.net/create_issue
