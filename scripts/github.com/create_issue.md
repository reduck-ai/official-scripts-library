# Create a GitHub issue

Automatically create a GitHub issue on github.com. Open a new issue in a GitHub repository as the signed-in account, with a title and an optional Markdown body, through the repository's own New issue form. Returns the new issue's number and link, confirmed in the repository's issue list. The account needs permission to open issues there, and the repository must have issues turned on.

- Site: github.com
- Address: `reduck/github.com/create_issue`
- Updated: 2026-11-04 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/github.com/create_issue`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/github.com/create_issue
```

## Input

- `repo` (string, required): Repository as owner/name, or its GitHub link.
- `title` (string, required): The issue's title.
- `body` (string, optional): The issue's description, in GitHub Markdown.

## Output

- `url` (string, required)
- `repo` (string, required)
- `title` (string, required): The title as GitHub lists it.
- `number` (integer, required)
- `verified` (boolean, required): True when the new issue is in the repository's issue list with the given title.

## FAQ

### What does "Create a GitHub issue" do?

Open a new issue in a GitHub repository as the signed-in account, with a title and an optional Markdown body, through the repository's own New issue form. Returns the new issue's number and link, confirmed in the repository's issue list. The account needs permission to open issues there, and the repository must have issues turned on.

### How do I automatically create a GitHub issue on github.com?

Ask an AI agent connected to Reduck to run reduck/github.com/create_issue, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/github.com/create_issue

### Is there a github.com API to create a GitHub issue?

You do not need one. "Create a GitHub issue" drives the real github.com pages in a browser, so it works whether or not github.com offers an API for this.

### What information do I need to provide?

Required: repo, title. Optional: body.

### What does it return?

It returns url, repo, title, number, verified.

### Do I need to be logged in to github.com?

Yes. It acts as you on github.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the github.com cookies saved by the Reduck extension.

### Does it change anything on github.com, or only read data?

It makes changes on github.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/github.com/create_issue, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/github.com/create_issue

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/github.com/create_issue
