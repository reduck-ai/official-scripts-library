# Unsubscribe from Substack publication

Automatically unsubscribe from Substack publication on substack.com. Unsubscribe the logged-in account from a Substack publication.

- Site: substack.com
- Address: `reduck/substack.com/unsubscribe_publication`
- Updated: 2026-08-25 (v4)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/substack.com/unsubscribe_publication`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/substack.com/unsubscribe_publication
```

## Input

- `publicationUrl` (string, required): Base URL of the Substack publication, e.g. https://example.substack.com

## Output

- `unsubscribed` (boolean, required)
- `publicationId` (number, required)
- `publicationUrl` (string, required)
- `membershipState` (string | null, optional)

## FAQ

### What does "Unsubscribe from Substack publication" do?

Unsubscribe the logged-in account from a Substack publication.

### How do I automatically unsubscribe from Substack publication on substack.com?

Ask an AI agent connected to Reduck to run reduck/substack.com/unsubscribe_publication, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/substack.com/unsubscribe_publication

### Is there a substack.com API to unsubscribe from Substack publication?

You do not need one. "Unsubscribe from Substack publication" drives the real substack.com pages in a browser, so it works whether or not substack.com offers an API for this.

### What information do I need to provide?

Required: publicationUrl.

### What does it return?

It returns unsubscribed, publicationId, publicationUrl, membershipState.

### Do I need to be logged in to substack.com?

Yes. It acts as you on substack.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the substack.com cookies saved by the Reduck extension.

### Does it change anything on substack.com, or only read data?

It makes changes on substack.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/substack.com/unsubscribe_publication, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/substack.com/unsubscribe_publication

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/substack.com/unsubscribe_publication
