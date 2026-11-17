# Upload Slack text file

Automatically upload Slack text file on slack.com. Upload a text file/snippet (its content given inline) to a channel via Slack's file-upload flow. For sharing logs, code or notes; binary files are out of scope. Returns the file id, name and permalink. Requires login.

- Site: slack.com
- Address: `reduck/slack.com/upload_file`
- Updated: 2026-11-16 (v4)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/slack.com/upload_file`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/slack.com/upload_file
```

## Input

- `channel` (string, required): Channel id (C…/G…/D…). Get it from slack.com/list_channels.
- `content` (string, required): The text content of the file.
- `workspaceDomain` (string, required): Workspace host, e.g. acme.slack.com. Confirm with the user which workspace to target before running.
- `title` (string, optional): Name shown for the snippet. Defaults to filename.
- `comment` (string, optional): Optional message posted with the file.
- `filename` (string, optional): File name, e.g. 'notes.txt'.

## Output

- `id` (string, required)
- `ok` (boolean, required)
- `name` (string | null, optional)
- `title` (string | null, optional)
- `permalink` (string | null, optional)
- `workspace` (string, optional)

## FAQ

### What does "Upload Slack text file" do?

Upload a text file/snippet (its content given inline) to a channel via Slack's file-upload flow. For sharing logs, code or notes; binary files are out of scope. Returns the file id, name and permalink. Requires login.

### How do I automatically upload Slack text file on slack.com?

Ask an AI agent connected to Reduck to run reduck/slack.com/upload_file, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/slack.com/upload_file

### Is there a slack.com API to upload Slack text file?

You do not need one. "Upload Slack text file" drives the real slack.com pages in a browser, so it works whether or not slack.com offers an API for this.

### What information do I need to provide?

Required: channel, content, workspaceDomain. Optional: title, comment, filename.

### What does it return?

It returns id, ok, name, title, permalink, workspace.

### Do I need to be logged in to slack.com?

Yes. It acts as you on slack.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the slack.com cookies saved by the Reduck extension.

### Does it change anything on slack.com, or only read data?

It makes changes on slack.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/slack.com/upload_file, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/slack.com/upload_file

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/slack.com/upload_file
