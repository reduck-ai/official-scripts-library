# Get LinkedIn connections

Automatically get LinkedIn connections on linkedin.com. List the logged-in member's 1st-degree LinkedIn connections (My Network > Connections), scrolling to load up to count. Returns each connection's name, headline, profile URL, member URN, and the "Connected on" date text, plus the total connection count LinkedIn reports.

- Site: linkedin.com
- Address: `reduck/linkedin.com/get_connections`
- Updated: 2026-09-03 (v5)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/linkedin.com/get_connections`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/linkedin.com/get_connections
```

## Input

- `count` (integer, optional): Max connections to return. Omit to fetch all of them.

## Output

- `total` (integer, required): Total connection count LinkedIn reports at the top of the list (may exceed connections.length if count capped it).
- `connections` (array, required)

## FAQ

### What does "Get LinkedIn connections" do?

List the logged-in member's 1st-degree LinkedIn connections (My Network > Connections), scrolling to load up to count. Returns each connection's name, headline, profile URL, member URN, and the "Connected on" date text, plus the total connection count LinkedIn reports.

### How do I automatically get LinkedIn connections on linkedin.com?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/get_connections, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/get_connections

### Is there a linkedin.com API to get LinkedIn connections?

You do not need one. "Get LinkedIn connections" drives the real linkedin.com pages in a browser, so it works whether or not linkedin.com offers an API for this.

### What information do I need to provide?

Optional: count.

### What does it return?

It returns total, connections.

### Do I need to be logged in to linkedin.com?

Yes. It acts as you on linkedin.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the linkedin.com cookies saved by the Reduck extension.

### Does it change anything on linkedin.com, or only read data?

It only reads. It looks things up on linkedin.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/linkedin.com/get_connections, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/linkedin.com/get_connections

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/linkedin.com/get_connections
