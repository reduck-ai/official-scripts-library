# Get Behance project

Automatically get Behance project on behance.net. Fetch a Behance project's details from its gallery URL: title, description, creators, tags, images, likes and views.

- Site: behance.net
- Address: `reduck/behance.net/get_project`
- Updated: 2026-08-28 (v6)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/behance.net/get_project`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/behance.net/get_project
```

## Input

- `url` (string, required): Full Behance gallery URL, e.g. https://www.behance.net/gallery/249279045/PUMA-Forever-Faster

## Output

- `id` (integer | null, required)
- `url` (string | null, required)
- `tags` (array, required): Canonical English category names (read from the tag links' `field=` URL param), not affected by the account's UI language.
- `likes` (integer | null, required)
- `title` (string | null, required)
- `views` (integer | null, required)
- `images` (array, required)
- `creators` (array, required)
- `coverImage` (string | null, required)
- `description` (string | null, required)

## FAQ

### What does "Get Behance project" do?

Fetch a Behance project's details from its gallery URL: title, description, creators, tags, images, likes and views.

### How do I automatically get Behance project on behance.net?

Ask an AI agent connected to Reduck to run reduck/behance.net/get_project, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/behance.net/get_project

### Is there a behance.net API to get Behance project?

You do not need one. "Get Behance project" drives the real behance.net pages in a browser, so it works whether or not behance.net offers an API for this.

### What information do I need to provide?

Required: url.

### What does it return?

It returns id, url, tags, likes, title, views, images, creators, coverImage, description.

### Do I need to be logged in to behance.net?

No. It only uses pages of behance.net that are reachable without signing in.

### Does it change anything on behance.net, or only read data?

It only reads. It looks things up on behance.net and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/behance.net/get_project, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/behance.net/get_project

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/behance.net/get_project
