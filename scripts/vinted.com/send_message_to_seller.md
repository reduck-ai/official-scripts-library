# Vinted — Send a message to an item's seller

Automatically send a message to an item's seller on vinted.com. Send a message to the seller of a Vinted listing, using the signed-in account's own "Ask seller" conversation composer on the item page.

- Site: vinted.com
- Address: `reduck/vinted.com/send_message_to_seller`
- Updated: 2026-09-18 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/vinted.com/send_message_to_seller`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/vinted.com/send_message_to_seller
```

## Input

- `itemUrl` (string, required): Full URL of the vinted.com/vinted.fr item listing to message the seller about, e.g. https://www.vinted.fr/items/9875508965-livre
- `message` (string, required): The message text to send to the seller.

## Output

- `sent` (boolean, required)
- `conversationUrl` (string, required)

## FAQ

### What does "Vinted — Send a message to an item's seller" do?

Send a message to the seller of a Vinted listing, using the signed-in account's own "Ask seller" conversation composer on the item page.

### How do I automatically send a message to an item's seller on vinted.com?

Ask an AI agent connected to Reduck to run reduck/vinted.com/send_message_to_seller, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/vinted.com/send_message_to_seller

### Is there a vinted.com API to send a message to an item's seller?

You do not need one. "Vinted — Send a message to an item's seller" drives the real vinted.com pages in a browser, so it works whether or not vinted.com offers an API for this.

### What information do I need to provide?

Required: itemUrl, message.

### What does it return?

It returns sent, conversationUrl.

### Do I need to be logged in to vinted.com?

Yes. It acts as you on vinted.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the vinted.com cookies saved by the Reduck extension.

### Does it change anything on vinted.com, or only read data?

It makes changes on vinted.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/vinted.com/send_message_to_seller, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/vinted.com/send_message_to_seller

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/vinted.com/send_message_to_seller
