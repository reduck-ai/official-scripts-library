# Search Google Drive

Automatically search Google Drive on drive.google.com. Search Google Drive by free text, or filter by name, file type, owner and modified-date range. Returns each match's file id, name, link and the folder it sits in. Drive's search results carry no sizes, types or dates, so filter by type rather than expecting those fields back, and use the folder listing script when you need full metadata.

- Site: drive.google.com
- Address: `reduck/drive.google.com/search_files`
- Updated: 2026-08-26 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/drive.google.com/search_files`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/drive.google.com/search_files
```

## Input

- `name` (string, optional): Restrict to files whose name contains these words.
- `type` (string, optional): Restrict to one Drive file type. Use this rather than filtering on mimeType afterwards — the search surface does not expose mimeTypes.
- `owner` (string, optional): Restrict by owner: an email address, or "me".
- `query` (string, optional): Free-text query, matched by Drive against file names and contents.
- `modifiedAfter` (string, optional): Only files modified on or after this date, as YYYY-MM-DD.
- `modifiedBefore` (string, optional): Only files modified before this date, as YYYY-MM-DD.

## Output

- `url` (string, required)
- `count` (number, required)
- `files` (array, required)
- `query` (string, required): The query string as submitted to Drive, including any operators built from the filters.
- `note` (string, optional): Present only when nothing was found, stating that Drive rendered no rows within the wait rather than implying a certain empty set.

## FAQ

### What does "Search Google Drive" do?

Search Google Drive by free text, or filter by name, file type, owner and modified-date range. Returns each match's file id, name, link and the folder it sits in. Drive's search results carry no sizes, types or dates, so filter by type rather than expecting those fields back, and use the folder listing script when you need full metadata.

### How do I automatically search Google Drive on drive.google.com?

Ask an AI agent connected to Reduck to run reduck/drive.google.com/search_files, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/drive.google.com/search_files

### Is there a drive.google.com API to search Google Drive?

You do not need one. "Search Google Drive" drives the real drive.google.com pages in a browser, so it works whether or not drive.google.com offers an API for this.

### What information do I need to provide?

Optional: name, type, owner, query, modifiedAfter, modifiedBefore.

### What does it return?

It returns url, note, count, files, query.

### Do I need to be logged in to drive.google.com?

Yes. It acts as you on drive.google.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the drive.google.com cookies saved by the Reduck extension.

### Does it change anything on drive.google.com, or only read data?

It only reads. It looks things up on drive.google.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/drive.google.com/search_files, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/drive.google.com/search_files

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/drive.google.com/search_files
