# WhatsApp — List communities

Automatically list communities on web.whatsapp.com. List the WhatsApp communities this account belongs to, each with the groups the Communities tab previews for it. Returns every community's name plus its group names, flagging the announcement group and whether WhatsApp is hiding further groups behind its "View all" link — the tab shows only the first few per community, so the group list is a preview rather than full membership. Returns an empty list when the account has no communities, which is a real answer rather than a failure.

- Site: web.whatsapp.com
- Address: `reduck/web.whatsapp.com/list_communities`
- Updated: 2026-09-03 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/web.whatsapp.com/list_communities`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/list_communities
```

## Input

It takes no input.

## Output

- `count` (integer, required): How many communities were found.
- `communities` (array, required): The communities this account belongs to, in the order the Communities tab lists them. Empty when there are none.

## FAQ

### What does "WhatsApp — List communities" do?

List the WhatsApp communities this account belongs to, each with the groups the Communities tab previews for it. Returns every community's name plus its group names, flagging the announcement group and whether WhatsApp is hiding further groups behind its "View all" link — the tab shows only the first few per community, so the group list is a preview rather than full membership. Returns an empty list when the account has no communities, which is a real answer rather than a failure.

### How do I automatically list communities on web.whatsapp.com?

Ask an AI agent connected to Reduck to run reduck/web.whatsapp.com/list_communities, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/list_communities

### Is there a web.whatsapp.com API to list communities?

You do not need one. "WhatsApp — List communities" drives the real web.whatsapp.com pages in a browser, so it works whether or not web.whatsapp.com offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns count, communities.

### Do I need to be logged in to web.whatsapp.com?

Yes. It acts as you on web.whatsapp.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the web.whatsapp.com cookies saved by the Reduck extension.

### Does it change anything on web.whatsapp.com, or only read data?

It only reads. It looks things up on web.whatsapp.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/web.whatsapp.com/list_communities, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/web.whatsapp.com/list_communities

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/web.whatsapp.com/list_communities
