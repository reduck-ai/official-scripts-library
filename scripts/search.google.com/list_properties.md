# List Google Search Console properties

Automatically list Google Search Console properties on search.google.com. Lists every Google Search Console property the signed-in Google account can open, both website (URL prefix) and Domain properties, with the account they were read from. Returns an empty list for an account with no properties. Pass a property's siteUrl to the other Search Console scripts.

- Site: search.google.com
- Address: `reduck/search.google.com/list_properties`
- Updated: 2026-10-07 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/search.google.com/list_properties`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/search.google.com/list_properties
```

## Input

It takes no input.

## Output

- `account` (string | null, required): Google account the console is signed in as.
- `properties` (array, required): Every property this account can open. Empty when the account has none.

## FAQ

### What does "List Google Search Console properties" do?

Lists every Google Search Console property the signed-in Google account can open, both website (URL prefix) and Domain properties, with the account they were read from. Returns an empty list for an account with no properties. Pass a property's siteUrl to the other Search Console scripts.

### How do I automatically list Google Search Console properties on search.google.com?

Ask an AI agent connected to Reduck to run reduck/search.google.com/list_properties, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/search.google.com/list_properties

### Is there a search.google.com API to list Google Search Console properties?

You do not need one. "List Google Search Console properties" drives the real search.google.com pages in a browser, so it works whether or not search.google.com offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns account, properties.

### Do I need to be logged in to search.google.com?

Yes. It acts as you on search.google.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the search.google.com cookies saved by the Reduck extension.

### Does it change anything on search.google.com, or only read data?

It only reads. It looks things up on search.google.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/search.google.com/list_properties, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/search.google.com/list_properties

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/search.google.com/list_properties
