# Get Pinterest pin details

Automatically get Pinterest pin details on pinterest.com. Fetches a single Pinterest pin's public details by id: title, description, image, creator, save/reaction counts, publish date, and (for link pins) the linked destination site. Read-only, no login required.

- Site: pinterest.com
- Address: `reduck/pinterest.com/get_pin`
- Updated: 2026-09-03 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/pinterest.com/get_pin`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/pinterest.com/get_pin
```

## Input

- `pinId` (string, required): Numeric Pinterest pin id, e.g. "9499849211132942"

## Output

- `id` (string, required)
- `url` (string, required)
- `title` (string | null, optional)
- `imageUrl` (string | null, optional)
- `saveCount` (integer | null, optional)
- `creatorUrl` (string | null, optional)
- `creatorName` (string | null, optional)
- `description` (string | null, optional)
- `linkedDomain` (string | null, optional)
- `creatorHandle` (string | null, optional)
- `datePublished` (string | null, optional)
- `reactionCount` (integer | null, optional)
- `destinationUrl` (string | null, optional)

## FAQ

### What does "Get Pinterest pin details" do?

Fetches a single Pinterest pin's public details by id: title, description, image, creator, save/reaction counts, publish date, and (for link pins) the linked destination site. Read-only, no login required.

### How do I automatically get Pinterest pin details on pinterest.com?

Ask an AI agent connected to Reduck to run reduck/pinterest.com/get_pin, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/pinterest.com/get_pin

### Is there a pinterest.com API to get Pinterest pin details?

You do not need one. "Get Pinterest pin details" drives the real pinterest.com pages in a browser, so it works whether or not pinterest.com offers an API for this.

### What information do I need to provide?

Required: pinId.

### What does it return?

It returns id, url, title, imageUrl, saveCount, creatorUrl, creatorName, description, linkedDomain, creatorHandle, datePublished, reactionCount, destinationUrl.

### Do I need to be logged in to pinterest.com?

No. It only uses pages of pinterest.com that are reachable without signing in.

### Does it change anything on pinterest.com, or only read data?

It only reads. It looks things up on pinterest.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/pinterest.com/get_pin, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/pinterest.com/get_pin

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/pinterest.com/get_pin
