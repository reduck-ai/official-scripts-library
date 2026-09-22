# Download brand logo pack

Automatically download brand logo pack on brandfetch.com. Given a company domain, opens its Brandfetch page and clicks "Download all" to save the full logo/icon/banner pack (SVG/PNG/WebP) to the local Downloads folder via the browser's native download.

- Site: brandfetch.com
- Address: `reduck/brandfetch.com/download_logo`
- Updated: 2026-08-17 (v4)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/brandfetch.com/download_logo`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/brandfetch.com/download_logo
```

## Input

- `domain` (string, required): Company domain, e.g. "apple.com", "canva.com", "spotify.com"

## Output

- `brand` (string | null, required): Clean display name of the brand, e.g. "Apple"; null when found is false
- `found` (boolean, required): false if Brandfetch has no page for this domain
- `domain` (string, required)
- `filename` (string | null, required): Suggested filename of the downloaded zip; null when found is false

## FAQ

### What does "Download brand logo pack" do?

Given a company domain, opens its Brandfetch page and clicks "Download all" to save the full logo/icon/banner pack (SVG/PNG/WebP) to the local Downloads folder via the browser's native download.

### How do I automatically download brand logo pack on brandfetch.com?

Ask an AI agent connected to Reduck to run reduck/brandfetch.com/download_logo, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/brandfetch.com/download_logo

### Is there a brandfetch.com API to download brand logo pack?

You do not need one. "Download brand logo pack" drives the real brandfetch.com pages in a browser, so it works whether or not brandfetch.com offers an API for this.

### What information do I need to provide?

Required: domain.

### What does it return?

It returns brand, found, domain, filename.

### Do I need to be logged in to brandfetch.com?

No. It only uses pages of brandfetch.com that are reachable without signing in.

### Does it change anything on brandfetch.com, or only read data?

It makes changes on brandfetch.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/brandfetch.com/download_logo, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/brandfetch.com/download_logo

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/brandfetch.com/download_logo
