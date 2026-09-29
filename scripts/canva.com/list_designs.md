# Canva — list designs

Automatically list designs on canva.com. List the designs on the signed-in Canva account's Projects page (most recent first, owned or shared with the account): design id, title, edit link, design type (e.g. Video, LinkedIn post, in the account's interface language), page count and creation date. Read-only. Returns the designs the Projects page loads on first view, not the full archive. Signed out is a clear error, not an empty list.

- Site: canva.com
- Address: `reduck/canva.com/list_designs`
- Updated: 2026-09-28 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/canva.com/list_designs`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/canva.com/list_designs
```

## Input

It takes no input.

## Output

- `count` (integer, required)
- `designs` (array, required)

## FAQ

### What does "Canva — list designs" do?

List the designs on the signed-in Canva account's Projects page (most recent first, owned or shared with the account): design id, title, edit link, design type (e.g. Video, LinkedIn post, in the account's interface language), page count and creation date. Read-only. Returns the designs the Projects page loads on first view, not the full archive. Signed out is a clear error, not an empty list.

### How do I automatically list designs on canva.com?

Ask an AI agent connected to Reduck to run reduck/canva.com/list_designs, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/canva.com/list_designs

### Is there a canva.com API to list designs?

You do not need one. "Canva — list designs" drives the real canva.com pages in a browser, so it works whether or not canva.com offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns count, designs.

### Do I need to be logged in to canva.com?

Yes. It acts as you on canva.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the canva.com cookies saved by the Reduck extension.

### Does it change anything on canva.com, or only read data?

It only reads. It looks things up on canva.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/canva.com/list_designs, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/canva.com/list_designs

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/canva.com/list_designs
