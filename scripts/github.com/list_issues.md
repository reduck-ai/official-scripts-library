# List GitHub issues

Automatically list GitHub issues on github.com. List the issues of a GitHub repository the signed-in account can see, as the repository's Issues tab shows them, 25 per page: number, title, state, author, dates and link, plus the total and the number of pages. Filter with GitHub's own search syntax (for example "is:open label:bug assignee:octocat"). Works on private repositories the account can open.

- Site: github.com
- Address: `reduck/github.com/list_issues`
- Updated: 2026-11-04 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/github.com/list_issues`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/github.com/list_issues
```

## Input

- `repo` (string, required): Repository as owner/name, or its GitHub link.
- `page` (integer, optional): Page of results, 25 per page.
- `query` (string, optional): GitHub issue search, as typed in the Issues tab's search box (is:open, is:closed, label:bug, author:..., assignee:..., sort:updated-desc). is:issue is added for you.

## Output

- `page` (integer, required)
- `repo` (string, required)
- `query` (string, required): The search GitHub ran.
- `total` (integer | null, required): How many issues match.
- `issues` (array, required)
- `totalPages` (integer | null, required): How many pages of 25 the matches fill; pass page to read the next.

## FAQ

### What does "List GitHub issues" do?

List the issues of a GitHub repository the signed-in account can see, as the repository's Issues tab shows them, 25 per page: number, title, state, author, dates and link, plus the total and the number of pages. Filter with GitHub's own search syntax (for example "is:open label:bug assignee:octocat"). Works on private repositories the account can open.

### How do I automatically list GitHub issues on github.com?

Ask an AI agent connected to Reduck to run reduck/github.com/list_issues, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/github.com/list_issues

### Is there a github.com API to list GitHub issues?

You do not need one. "List GitHub issues" drives the real github.com pages in a browser, so it works whether or not github.com offers an API for this.

### What information do I need to provide?

Required: repo. Optional: page, query.

### What does it return?

It returns page, repo, query, total, issues, totalPages.

### Do I need to be logged in to github.com?

Yes. It acts as you on github.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the github.com cookies saved by the Reduck extension.

### Does it change anything on github.com, or only read data?

It only reads. It looks things up on github.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/github.com/list_issues, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/github.com/list_issues

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/github.com/list_issues
