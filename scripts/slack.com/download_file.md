# Download a file from Slack

Automatically download a file from Slack on slack.com. Downloads a file stored in Slack to the machine running the browser, taking the file's ID or its Slack link, and reports where it was saved along with the file's name, type and size.

- Site: slack.com
- Address: `reduck/slack.com/download_file`
- Updated: 2026-09-23 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/slack.com/download_file`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/slack.com/download_file
```

## Input

- `file` (string, required): The file's Slack ID (for example F01234ABCDE) or its Slack file link. A link must belong to the same workspace as workspaceDomain.
- `workspaceDomain` (string, required): Workspace hostname, for example acme.slack.com.
- `expectedUser` (string, optional): Optional guard. Your Slack handle, display name, or user ID. When given, it is checked against the signed-in account and the download is refused on a mismatch.

## Output

- `file` (object, required)
- `account` (object, required)
- `download` (object, required)
- `workspace` (string, required)

## FAQ

### What does "Download a file from Slack" do?

Downloads a file stored in Slack to the machine running the browser, taking the file's ID or its Slack link, and reports where it was saved along with the file's name, type and size.

### How do I automatically download a file from Slack on slack.com?

Ask an AI agent connected to Reduck to run reduck/slack.com/download_file, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/slack.com/download_file

### Is there a slack.com API to download a file from Slack?

You do not need one. "Download a file from Slack" drives the real slack.com pages in a browser, so it works whether or not slack.com offers an API for this.

### What information do I need to provide?

Required: workspaceDomain, file. Optional: expectedUser.

### What does it return?

It returns file, account, download, workspace.

### Do I need to be logged in to slack.com?

Yes. It acts as you on slack.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the slack.com cookies saved by the Reduck extension.

### Does it change anything on slack.com, or only read data?

It only reads. It looks things up on slack.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/slack.com/download_file, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/slack.com/download_file

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/slack.com/download_file
