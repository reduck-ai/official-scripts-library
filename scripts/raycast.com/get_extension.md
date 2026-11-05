# Raycast — get Store extension

Automatically get Store extension on raycast.com. Get one Raycast Store extension from its Store URL parts (raycast.com/<author>/<name>): title, description, canonical Store URL, author, owning organization, downloads, status, platforms, categories, contributors, every command (name, title, description), and created / updated dates. Public data, no sign-in needed. Use the handle that is in the Store URL: for an extension owned by an organization, that is the organization (e.g. raycast/github), not the person who wrote it. An unknown author/name pair is a clear error.

- Site: raycast.com
- Address: `reduck/raycast.com/get_extension`
- Updated: 2026-11-04 (v6)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/raycast.com/get_extension`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/raycast.com/get_extension
```

## Input

- `name` (string, required): The extension's slug, the last part of its Store URL (e.g. "github" for raycast.com/raycast/github).
- `author` (string, required): The author or owner handle, the first part of its Store URL (e.g. "raycast" for raycast.com/raycast/github).

## Output

- `id` (string, required)
- `url` (string, required): The canonical Store URL (may be under the owning organization).
- `name` (string, required)
- `owner` (string | null, optional)
- `title` (string | null, optional)
- `author` (string | null, optional)
- `status` (string | null, optional)
- `commands` (array, optional)
- `createdAt` (string | null, optional)
- `downloads` (integer | null, optional)
- `platforms` (array, optional)
- `updatedAt` (string | null, optional)
- `authorName` (string | null, optional)
- `categories` (array, optional)
- `description` (string | null, optional)
- `contributors` (array, optional)

## FAQ

### What does "Raycast — get Store extension" do?

Get one Raycast Store extension from its Store URL parts (raycast.com/<author>/<name>): title, description, canonical Store URL, author, owning organization, downloads, status, platforms, categories, contributors, every command (name, title, description), and created / updated dates. Public data, no sign-in needed. Use the handle that is in the Store URL: for an extension owned by an organization, that is the organization (e.g. raycast/github), not the person who wrote it. An unknown author/name pair is a clear error.

### How do I automatically get Store extension on raycast.com?

Ask an AI agent connected to Reduck to run reduck/raycast.com/get_extension, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/raycast.com/get_extension

### Is there a raycast.com API to get Store extension?

You do not need one. "Raycast — get Store extension" drives the real raycast.com pages in a browser, so it works whether or not raycast.com offers an API for this.

### What information do I need to provide?

Required: name, author.

### What does it return?

It returns id, url, name, owner, title, author, status, commands, createdAt, downloads, platforms, updatedAt, authorName, categories, description, contributors.

### Do I need to be logged in to raycast.com?

No. It only uses pages of raycast.com that are reachable without signing in.

### Does it change anything on raycast.com, or only read data?

It only reads. It looks things up on raycast.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/raycast.com/get_extension, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/raycast.com/get_extension

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/raycast.com/get_extension
