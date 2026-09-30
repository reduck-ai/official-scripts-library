# Download a Qonto bank statement

Automatically download a Qonto bank statement on qonto.com. Download a monthly account statement PDF from the signed-in Qonto business account. Pass month as YYYY-MM, or omit it for the latest statement. The PDF is saved as qonto-statement-YYYY-MM.pdf. Returns where it was saved, its size, and the list of every statement month available. It checks the file really is a PDF before reporting success, and if the month does not exist it fails with the list of available months instead of downloading something else. Read-only on Qonto.

- Site: qonto.com
- Address: `reduck/qonto.com/download_statement`
- Updated: 2026-09-29 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/qonto.com/download_statement`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/qonto.com/download_statement
```

## Input

- `month` (string, optional): Statement month as YYYY-MM (e.g. 2026-08). Omit for the most recent statement.

## Output

- `bytes` (integer, required)
- `filename` (string, required)
- `statement` (string, required): YYYY-MM of the downloaded statement.
- `url` (string | null, optional): Link to the file when it is not on that machine.
- `path` (string | null, optional): Where the PDF was saved on the machine running the browser.
- `available` (array, optional): All statement months on the account, newest first.
- `statementId` (string, optional)

## FAQ

### What does "Download a Qonto bank statement" do?

Download a monthly account statement PDF from the signed-in Qonto business account. Pass month as YYYY-MM, or omit it for the latest statement. The PDF is saved as qonto-statement-YYYY-MM.pdf. Returns where it was saved, its size, and the list of every statement month available. It checks the file really is a PDF before reporting success, and if the month does not exist it fails with the list of available months instead of downloading something else. Read-only on Qonto.

### How do I automatically download a Qonto bank statement on qonto.com?

Ask an AI agent connected to Reduck to run reduck/qonto.com/download_statement, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/qonto.com/download_statement

### Is there a qonto.com API to download a Qonto bank statement?

You do not need one. "Download a Qonto bank statement" drives the real qonto.com pages in a browser, so it works whether or not qonto.com offers an API for this.

### What information do I need to provide?

Optional: month.

### What does it return?

It returns url, path, bytes, filename, available, statement, statementId.

### Do I need to be logged in to qonto.com?

Yes. It acts as you on qonto.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the qonto.com cookies saved by the Reduck extension.

### Does it change anything on qonto.com, or only read data?

It only reads. It looks things up on qonto.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/qonto.com/download_statement, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/qonto.com/download_statement

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/qonto.com/download_statement
