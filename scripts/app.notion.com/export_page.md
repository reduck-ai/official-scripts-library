# Export a Notion page to PDF, HTML or Markdown

Automatically export a Notion page to PDF, HTML or Markdown on app.notion.com. Export a Notion page from its URL and save the file to the browser machine's downloads folder. Choose PDF, HTML or Markdown, and optionally include the page's subpages. Returns the saved file's name, its path (or a link on a managed browser) and the page title. Markdown and HTML exports arrive as a zip archive; a PDF export of a single page arrives as a PDF named after the page. Asking for subpages in a format the workspace's plan does not allow fails with an error saying so. A signed-out browser fails with a signed-out error asking to sign in to notion.com.

- Site: app.notion.com
- Address: `reduck/app.notion.com/export_page`
- Updated: 2026-10-22 (v6)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/app.notion.com/export_page`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/app.notion.com/export_page
```

## Input

- `url` (string, required): The Notion page URL, as copied from the browser or from Copy link (for example https://www.notion.so/My-Page-2b6da534361881e580d5f4cf4a8c36bd).
- `format` (string, optional): Export format. markdown and html produce a zip archive; pdf produces a PDF file. Including subpages in a PDF requires a Business plan; on other plans that toggle is locked and a pdf export covers the page alone.
- `include_subpages` (boolean, optional): Include the page's subpages in the export. When false only the page itself is exported. Requesting true for a pdf export on a plan that locks the setting fails with a clear error rather than silently exporting one page.

## Output

- `url` (string | null, required): A link to the file's bytes on a managed browser. Null on the user's Chrome.
- `path` (string | null, required): Absolute path of the saved file on the machine running the browser. Null on a managed browser.
- `format` (string, required): The format the export was requested in.
- `filename` (string, required): The saved file's name: a zip for markdown and html exports, a PDF named after the page for pdf exports. It can end in (2) when a file of that name was already there.
- `page_url` (string, required): The page URL the export ran against, after any redirect.
- `page_title` (string, required): Title of the exported page.
- `include_subpages` (boolean, required): Whether subpages were actually included, read back from the dialog rather than assumed from the argument. False when the workspace's plan locks the setting.
- `subpages_control` (string, required): set when the script chose the subpage setting; locked_by_plan when Notion disabled the toggle for this format on this workspace's plan, in which case subpages are not included.

## FAQ

### What does "Export a Notion page to PDF, HTML or Markdown" do?

Export a Notion page from its URL and save the file to the browser machine's downloads folder. Choose PDF, HTML or Markdown, and optionally include the page's subpages. Returns the saved file's name, its path (or a link on a managed browser) and the page title. Markdown and HTML exports arrive as a zip archive; a PDF export of a single page arrives as a PDF named after the page. Asking for subpages in a format the workspace's plan does not allow fails with an error saying so. A signed-out browser fails with a signed-out error asking to sign in to notion.com.

### How do I automatically export a Notion page to PDF, HTML or Markdown on app.notion.com?

Ask an AI agent connected to Reduck to run reduck/app.notion.com/export_page, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/app.notion.com/export_page

### Is there a app.notion.com API to export a Notion page to PDF, HTML or Markdown?

You do not need one. "Export a Notion page to PDF, HTML or Markdown" drives the real app.notion.com pages in a browser, so it works whether or not app.notion.com offers an API for this.

### What information do I need to provide?

Required: url. Optional: format, include_subpages.

### What does it return?

It returns url, path, format, filename, page_url, page_title, include_subpages, subpages_control.

### Do I need to be logged in to app.notion.com?

Yes. It acts as you on app.notion.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the app.notion.com cookies saved by the Reduck extension.

### Does it change anything on app.notion.com, or only read data?

It only reads. It looks things up on app.notion.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/app.notion.com/export_page, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/app.notion.com/export_page

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/app.notion.com/export_page
