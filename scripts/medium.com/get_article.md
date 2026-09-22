# Get Medium article details

Automatically get Medium article details on medium.com. Fetch a Medium article's metadata: title, description, author, publication, published date, tags, read time, and whether it's free to read. No login required.

- Site: medium.com
- Address: `reduck/medium.com/get_article`
- Updated: 2026-09-02 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/medium.com/get_article`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/medium.com/get_article
```

## Input

- `url` (string, required): Full Medium article URL, e.g. "https://medium.com/the-conscious-path/the-fermi-paradox-is-not-the-question-e67f967f4a21"

## Output

- `url` (string, required)
- `available` (boolean, required)
- `tags` (array, optional)
- `title` (string | null, optional)
- `imageUrl` (string | null, optional)
- `authorUrl` (string | null, optional)
- `authorName` (string | null, optional)
- `description` (string | null, optional)
- `datePublished` (string | null, optional)
- `publicationUrl` (string | null, optional)
- `publicationName` (string | null, optional)
- `readTimeMinutes` (integer | null, optional)
- `isAccessibleForFree` (boolean | null, optional)

## FAQ

### What does "Get Medium article details" do?

Fetch a Medium article's metadata: title, description, author, publication, published date, tags, read time, and whether it's free to read. No login required.

### How do I automatically get Medium article details on medium.com?

Ask an AI agent connected to Reduck to run reduck/medium.com/get_article, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/medium.com/get_article

### Is there a medium.com API to get Medium article details?

You do not need one. "Get Medium article details" drives the real medium.com pages in a browser, so it works whether or not medium.com offers an API for this.

### What information do I need to provide?

Required: url.

### What does it return?

It returns url, tags, title, imageUrl, authorUrl, available, authorName, description, datePublished, publicationUrl, publicationName, readTimeMinutes, isAccessibleForFree.

### Do I need to be logged in to medium.com?

No. It only uses pages of medium.com that are reachable without signing in.

### Does it change anything on medium.com, or only read data?

It only reads. It looks things up on medium.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/medium.com/get_article, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/medium.com/get_article

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/medium.com/get_article
