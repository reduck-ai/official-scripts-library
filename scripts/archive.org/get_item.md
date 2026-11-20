# Get Internet Archive item

Automatically get Internet Archive item on archive.org. Read one Internet Archive item by its identifier (from search_items or an archive.org/details URL): title, creator, date, description, subjects, collections, and every file with its format, size and direct download URL. Fails with a clear message when the identifier does not exist or the item is not public.

- Site: archive.org
- Address: `reduck/archive.org/get_item`
- Updated: 2026-11-19 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/archive.org/get_item`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/archive.org/get_item
```

## Input

- `identifier` (string, required): Item identifier, e.g. 'night_of_the_living_dead_dvd', or a full archive.org/details URL.

## Output

- `url` (string, required)
- `files` (array, required)
- `identifier` (string, required)
- `date` (string | null, optional)
- `title` (string | null, optional)
- `creator` (string | null, optional)
- `license` (string | null, optional)
- `subjects` (array, optional)
- `item_size` (integer | null, optional)
- `mediatype` (string | null, optional)
- `collections` (array, optional)
- `description` (string | null, optional)

## FAQ

### What does "Get Internet Archive item" do?

Read one Internet Archive item by its identifier (from search_items or an archive.org/details URL): title, creator, date, description, subjects, collections, and every file with its format, size and direct download URL. Fails with a clear message when the identifier does not exist or the item is not public.

### How do I automatically get Internet Archive item on archive.org?

Ask an AI agent connected to Reduck to run reduck/archive.org/get_item, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/archive.org/get_item

### Is there a archive.org API to get Internet Archive item?

You do not need one. "Get Internet Archive item" drives the real archive.org pages in a browser, so it works whether or not archive.org offers an API for this.

### What information do I need to provide?

Required: identifier.

### What does it return?

It returns url, date, files, title, creator, license, subjects, item_size, mediatype, identifier, collections, description.

### Do I need to be logged in to archive.org?

No. It only uses pages of archive.org that are reachable without signing in.

### Does it change anything on archive.org, or only read data?

It only reads. It looks things up on archive.org and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/archive.org/get_item, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/archive.org/get_item

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/archive.org/get_item
