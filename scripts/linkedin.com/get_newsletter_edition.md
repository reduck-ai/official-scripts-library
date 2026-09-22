# Get LinkedIn newsletter edition

Automatically get LinkedIn newsletter edition on linkedin.com. Fetch a single LinkedIn newsletter edition (article) by its permalink. Returns the newsletter it belongs to, the author, publish date, cover image, the full body converted to Markdown, and engagement stats (reactions, comments, reposts). Use get_edition_reactors for who reacted and get_edition_comments for the comment thread.

- Site: linkedin.com
- Address: `reduck/linkedin.com/get_newsletter_edition`
- Updated: 2026-09-08 (v7)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/linkedin.com/get_newsletter_edition`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/linkedin.com/get_newsletter_edition
```

## Input

- `editionUrl` (string, required): LinkedIn newsletter edition permalink, e.g. https://www.linkedin.com/pulse/<slug>-<code>/. Query string is stripped.

## Output

- `url` (string, required)
- `title` (string, required)
- `contentMarkdown` (string, required): The edition body converted to Markdown (headings, paragraphs, lists, bold/italic, links, images).
- `stats` (object, optional)
- `author` (object, optional)
- `articleUrn` (string | null, optional): urn:li:linkedInArticle:<id> read from the page, the edition's own identity. Null only if the marker isn't present.
- `newsletter` (object, optional)
- `publishedAt` (string | null, optional): Publish date as rendered, e.g. 'August 19, 2026'.
- `coverImageUrl` (string | null, optional)

## FAQ

### What does "Get LinkedIn newsletter edition" do?

Fetch a single LinkedIn newsletter edition (article) by its permalink. Returns the newsletter it belongs to, the author, publish date, cover image, the full body converted to Markdown, and engagement stats (reactions, comments, reposts). Use get_edition_reactors for who reacted and get_edition_comments for the comment thread.

### How do I automatically get LinkedIn newsletter edition on linkedin.com?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/get_newsletter_edition, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/get_newsletter_edition

### Is there a linkedin.com API to get LinkedIn newsletter edition?

You do not need one. "Get LinkedIn newsletter edition" drives the real linkedin.com pages in a browser, so it works whether or not linkedin.com offers an API for this.

### What information do I need to provide?

Required: editionUrl.

### What does it return?

It returns url, stats, title, author, articleUrn, newsletter, publishedAt, coverImageUrl, contentMarkdown.

### Do I need to be logged in to linkedin.com?

Yes. It acts as you on linkedin.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the linkedin.com cookies saved by the Reduck extension.

### Does it change anything on linkedin.com, or only read data?

It only reads. It looks things up on linkedin.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/get_newsletter_edition, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/get_newsletter_edition

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/linkedin.com/get_newsletter_edition
