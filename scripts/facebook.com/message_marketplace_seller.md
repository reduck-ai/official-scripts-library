# Message a Facebook Marketplace seller

Open a Facebook Marketplace listing's message box as the signed-in account and type a message to its seller. With send false (the default) the message is typed and left unsent, and the script returns what the box holds; with send true it is sent. A listing you cannot message (your own, removed, or messaging off) returns an error.

- Site: facebook.com
- Address: `reduck/facebook.com/message_marketplace_seller`
- Updated: 2026-11-05 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/facebook.com/message_marketplace_seller`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/facebook.com/message_marketplace_seller
```

## Input

- `listing` (string, required): Listing id or item link, from search_marketplace_listings.
- `message` (string, required)
- `send` (boolean, optional): false types the message without sending it.

## Output

- `sent` (boolean, required)
- `listingId` (string, required)
- `sellerName` (string | null, required)
- `typedMessage` (string | null, required)

## FAQ

### What does "Message a Facebook Marketplace seller" do?

Open a Facebook Marketplace listing's message box as the signed-in account and type a message to its seller. With send false (the default) the message is typed and left unsent, and the script returns what the box holds; with send true it is sent. A listing you cannot message (your own, removed, or messaging off) returns an error.

### What information do I need to provide?

Required: listing, message. Optional: send.

### What does it return?

It returns sent, listingId, sellerName, typedMessage.

### Do I need to be logged in to facebook.com?

Yes. It acts as you on facebook.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the facebook.com cookies saved by the Reduck extension.

### Does it change anything on facebook.com, or only read data?

It makes changes on facebook.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/facebook.com/message_marketplace_seller, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/facebook.com/message_marketplace_seller

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/facebook.com/message_marketplace_seller
