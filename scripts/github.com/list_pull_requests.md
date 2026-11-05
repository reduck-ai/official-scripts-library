# List GitHub pull requests

Automatically list GitHub pull requests on github.com. List the pull requests of a GitHub repository the signed-in account can see, as its Pull requests tab shows them, 25 per page: number, title, state (open, closed, merged or draft), author, dates, link and head commit, plus the total and how many are open and closed. Filter with GitHub's own search syntax (for example "is:open author:octocat review:required"). Works on private repositories the account can open.

- Site: github.com
- Address: `reduck/github.com/list_pull_requests`
- Updated: 2026-11-04 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/github.com/list_pull_requests`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/github.com/list_pull_requests
```

## Input

- `repo` (string, required): Repository as owner/name, or its GitHub link.
- `page` (integer, optional): Page of results, 25 per page.
- `query` (string, optional): GitHub pull request search, as typed in the Pull requests tab's search box (is:open, is:merged, is:draft, author:..., review:required, sort:updated-desc). is:pr is added for you.

## Output

- `page` (integer, required)
- `repo` (string, required)
- `query` (string, required): The search GitHub ran.
- `total` (integer | null, required): How many pull requests match.
- `openCount` (integer | null, required): Open pull requests among the matches, as the tab's Open count.
- `totalPages` (integer | null, required)
- `closedCount` (integer | null, required)
- `pullRequests` (array, required)

## FAQ

### What does "List GitHub pull requests" do?

List the pull requests of a GitHub repository the signed-in account can see, as its Pull requests tab shows them, 25 per page: number, title, state (open, closed, merged or draft), author, dates, link and head commit, plus the total and how many are open and closed. Filter with GitHub's own search syntax (for example "is:open author:octocat review:required"). Works on private repositories the account can open.

### How do I automatically list GitHub pull requests on github.com?

Ask an AI agent connected to Reduck to run reduck/github.com/list_pull_requests, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/github.com/list_pull_requests

### Is there a github.com API to list GitHub pull requests?

You do not need one. "List GitHub pull requests" drives the real github.com pages in a browser, so it works whether or not github.com offers an API for this.

### What information do I need to provide?

Required: repo. Optional: page, query.

### What does it return?

It returns page, repo, query, total, openCount, totalPages, closedCount, pullRequests.

### Do I need to be logged in to github.com?

Yes. It acts as you on github.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the github.com cookies saved by the Reduck extension.

### Does it change anything on github.com, or only read data?

It only reads. It looks things up on github.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/github.com/list_pull_requests, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/github.com/list_pull_requests

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/github.com/list_pull_requests
