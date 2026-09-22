# Create OAuth client (Web application)

Automatically create OAuth client (Web application) on console.cloud.google.com. An unofficial Google Cloud API: create a web OAuth client and get its id and secret programmatically, from code or from an AI agent, with typed JSON in and out. Google offers no API to create a standard web OAuth client; it is console-only.

- Site: console.cloud.google.com
- Address: `reduck/console.cloud.google.com/create_oauth_client`
- Updated: 2026-08-31 (v12)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/console.cloud.google.com/create_oauth_client`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/console.cloud.google.com/create_oauth_client
```

## Input

- `name` (string, required): Display name for the OAuth client (console-only label)
- `account` (string, required): Google account the client is created under. Must be the browser session's DEFAULT (authuser=0) account - the script verifies this and fails loud on a mismatch; it does not switch accounts.
- `projectId` (string, required): GCP project id that owns the OAuth consent screen, e.g. gen-lang-client-0289504322
- `redirectUris` (array, required): Authorised redirect URIs, e.g. https://your-app.vercel.app/auth/callback/google

## Output

- `name` (string, required)
- `clientId` (string, required)
- `clientSecret` (string, required): Shown only at creation; store it now

## FAQ

### What does "Create OAuth client (Web application)" do?

Create a Web-application OAuth 2.0 client in the Google Cloud Console (Google Auth Platform) for a project and return its clientId + clientSecret. Returns the full credential, including the client secret (the success dialog itself only shows the id). Requires the browser to already be signed in to Google, and a pre-existing OAuth consent screen for the project.

### How do I automatically create OAuth client (Web application) on console.cloud.google.com?

Ask an AI agent connected to Reduck to run reduck/console.cloud.google.com/create_oauth_client, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/console.cloud.google.com/create_oauth_client

### Is there a console.cloud.google.com API to create OAuth client (Web application)?

You do not need one. "Create OAuth client (Web application)" drives the real console.cloud.google.com pages in a browser, so it works whether or not console.cloud.google.com offers an API for this.

### What information do I need to provide?

Required: account, projectId, name, redirectUris.

### What does it return?

It returns name, clientId, clientSecret.

### Do I need to be logged in to console.cloud.google.com?

Yes. It acts as you on console.cloud.google.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the console.cloud.google.com cookies saved by the Reduck extension.

### Does it change anything on console.cloud.google.com, or only read data?

It makes changes on console.cloud.google.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/console.cloud.google.com/create_oauth_client, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/console.cloud.google.com/create_oauth_client

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/console.cloud.google.com/create_oauth_client
