# Sheets: new spreadsheet

Create a new Google Spreadsheet in My Drive, optionally with a title. Returns spreadsheetId, url, and firstGid (always 0). The file lands in Drive root (My Drive); moving it elsewhere is a Drive action, not a Sheets one.

- Site: docs.google.com
- Address: `reduck/docs.google.com/sheets_new_spreadsheet`
- Updated: 2026-09-07 (v5)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/docs.google.com/sheets_new_spreadsheet`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/docs.google.com/sheets_new_spreadsheet
```

## Input

- `title` (string, optional): Optional title. Omit (or pass only whitespace) to keep Google's default "Untitled spreadsheet", whose wording depends on the account's language.

## Output

- `url` (string, required)
- `firstGid` (string, required)
- `spreadsheetId` (string, required)
- `title` (string | null, optional): The spreadsheet's name, read back off a freshly reloaded editor so it reflects what Google saved rather than what was typed. Null when no title was requested.
- `rename_attempts` (integer, optional): How many times the title had to be filled before it stuck. More than 1 means the editor discarded the first attempt.

## FAQ

### What does "Sheets: new spreadsheet" do?

Create a new Google Spreadsheet in My Drive, optionally with a title. Returns spreadsheetId, url, and firstGid (always 0). The file lands in Drive root (My Drive); moving it elsewhere is a Drive action, not a Sheets one.

### What information do I need to provide?

Optional: title.

### What does it return?

It returns url, title, firstGid, spreadsheetId, rename_attempts.

### Do I need to be logged in to docs.google.com?

Yes. It acts as you on docs.google.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the docs.google.com cookies saved by the Reduck extension.

### Does it change anything on docs.google.com, or only read data?

It makes changes on docs.google.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/docs.google.com/sheets_new_spreadsheet, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/docs.google.com/sheets_new_spreadsheet

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/docs.google.com/sheets_new_spreadsheet
