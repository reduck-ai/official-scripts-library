# Delete OAuth client

Automatically delete OAuth client on console.cloud.google.com. Delete an OAuth 2.0 client from the Google Cloud Console (Google Auth Platform) by its client id. Needs console.cloud.google.com cookies (loggedIn). Deletion is immediate but the client can be restored for 30 days from the console's "Restore deleted OAuth clients" page.

- Site: console.cloud.google.com
- Address: `reduck/console.cloud.google.com/delete_oauth_client`
- Updated: 2026-08-28 (v4)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/console.cloud.google.com/delete_oauth_client`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/console.cloud.google.com/delete_oauth_client
```

## Input

- `clientId` (string, required): Full OAuth client id, e.g. 69462188880-abc123.apps.googleusercontent.com — as returned by create_oauth_client or shown on the client's own console page
- `projectId` (string, required): GCP project id that owns the OAuth client, e.g. testing-e2e-483713

## Output

- `clientId` (string, required)

## FAQ

### What does "Delete OAuth client" do?

Delete an OAuth 2.0 client from the Google Cloud Console (Google Auth Platform) by its client id. Needs console.cloud.google.com cookies (loggedIn). Deletion is immediate but the client can be restored for 30 days from the console's "Restore deleted OAuth clients" page.

### How do I automatically delete OAuth client on console.cloud.google.com?

Ask an AI agent connected to Reduck to run reduck/console.cloud.google.com/delete_oauth_client, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/console.cloud.google.com/delete_oauth_client

### Is there a console.cloud.google.com API to delete OAuth client?

You do not need one. "Delete OAuth client" drives the real console.cloud.google.com pages in a browser, so it works whether or not console.cloud.google.com offers an API for this.

### What information do I need to provide?

Required: projectId, clientId.

### What does it return?

It returns clientId.

### Do I need to be logged in to console.cloud.google.com?

Yes. It acts as you on console.cloud.google.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the console.cloud.google.com cookies saved by the Reduck extension.

### Does it change anything on console.cloud.google.com, or only read data?

It makes changes on console.cloud.google.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/console.cloud.google.com/delete_oauth_client, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/console.cloud.google.com/delete_oauth_client

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/console.cloud.google.com/delete_oauth_client
