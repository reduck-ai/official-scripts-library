# Search Google Drive

Automatically search Google Drive on drive.google.com. Search Google Drive by free text in names and contents, or filter by name, file type, owner and modified-date range. Returns each match's id, name, type, size, dates, owner, parent folders and link, one page at a time: pass nextPageToken back as pageToken to read the next page. No match returns an empty list.

- Site: drive.google.com
- Address: `reduck/drive.google.com/search_files`
- Updated: 2026-10-13 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/drive.google.com/search_files`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/drive.google.com/search_files
```

## Input

- `name` (string, optional): Only files whose name contains this text.
- `type` (string, optional): Only files of this type.
- `owner` (string, optional): Only files owned by this email address, or "me".
- `query` (string, optional): Free text, matched by Drive against file names and contents.
- `pageSize` (integer, optional): Number of results per page, up to 1000.
- `pageToken` (string, optional): The nextPageToken of the previous page, to read the next one.
- `modifiedAfter` (string, optional): Only files modified on or after this date, as YYYY-MM-DD.
- `modifiedBefore` (string, optional): Only files modified before this date, as YYYY-MM-DD.

## Output

- `count` (integer, required): Files on this page.
- `files` (array, required)
- `query` (string, required): The search as Drive received it.
- `nextPageToken` (string | null, required): Pass it as pageToken to read the next page. Null on the last page.

## FAQ

### What does "Search Google Drive" do?

Search Google Drive by free text in names and contents, or filter by name, file type, owner and modified-date range. Returns each match's id, name, type, size, dates, owner, parent folders and link, one page at a time: pass nextPageToken back as pageToken to read the next page. No match returns an empty list.

### How do I automatically search Google Drive on drive.google.com?

Ask an AI agent connected to Reduck to run reduck/drive.google.com/search_files, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/drive.google.com/search_files

### Is there a drive.google.com API to search Google Drive?

You do not need one. "Search Google Drive" drives the real drive.google.com pages in a browser, so it works whether or not drive.google.com offers an API for this.

### What information do I need to provide?

Optional: name, type, owner, query, pageSize, pageToken, modifiedAfter, modifiedBefore.

### What does it return?

It returns count, files, query, nextPageToken.

### Do I need to be logged in to drive.google.com?

Yes. It acts as you on drive.google.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the drive.google.com cookies saved by the Reduck extension.

### Does it change anything on drive.google.com, or only read data?

It only reads. It looks things up on drive.google.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/drive.google.com/search_files, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/drive.google.com/search_files

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/drive.google.com/search_files
