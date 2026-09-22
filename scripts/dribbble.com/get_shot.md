# Get Dribbble shot

Automatically get Dribbble shot on dribbble.com. Fetch a Dribbble shot's details from its url: title, description, owner, images and comment count.

- Site: dribbble.com
- Address: `reduck/dribbble.com/get_shot`
- Updated: 2026-08-25 (v4)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/dribbble.com/get_shot`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/dribbble.com/get_shot
```

## Input

- `url` (string, required): Full Dribbble shot URL, e.g. https://dribbble.com/shots/25843369-Logo-design-projects-2024-2025-portfolio

## Output

- `url` (string | null, required)
- `owner` (string | null, required)
- `title` (string | null, required)
- `images` (array, required)
- `ownerUrl` (string | null, required)
- `description` (string | null, required)
- `commentsCount` (integer | null, required)

## FAQ

### What does "Get Dribbble shot" do?

Fetch a Dribbble shot's details from its url: title, description, owner, images and comment count.

### How do I automatically get Dribbble shot on dribbble.com?

Ask an AI agent connected to Reduck to run reduck/dribbble.com/get_shot, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/dribbble.com/get_shot

### Is there a dribbble.com API to get Dribbble shot?

You do not need one. "Get Dribbble shot" drives the real dribbble.com pages in a browser, so it works whether or not dribbble.com offers an API for this.

### What information do I need to provide?

Required: url.

### What does it return?

It returns url, owner, title, images, ownerUrl, description, commentsCount.

### Do I need to be logged in to dribbble.com?

No. It only uses pages of dribbble.com that are reachable without signing in.

### Does it change anything on dribbble.com, or only read data?

It only reads. It looks things up on dribbble.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/dribbble.com/get_shot, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/dribbble.com/get_shot

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/dribbble.com/get_shot
