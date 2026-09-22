# Create X List

Automatically create X List on x.com. Creates a new X List with a name, optional description, and public/private visibility.

- Site: x.com
- Address: `reduck/x.com/create_list`
- Updated: 2026-09-08 (v6)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/x.com/create_list`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/x.com/create_list
```

## Input

- `name` (string, required): The List's display name. X caps this at 25 characters — the composer itself refuses more.
- `private` (boolean, optional): When true, only this account can see the List (its members and its posts). When false, it's public.
- `description` (string, optional): Optional description shown on the List's page. X caps this at 100 characters.

## Output

- `url` (string, required)
- `name` (string, required)
- `list_id` (string, required)
- `private` (boolean, required)
- `description` (string, optional)

## FAQ

### What does "Create X List" do?

Creates a new X List with a name, optional description, and public/private visibility.

### How do I automatically create X List on x.com?

Ask an AI agent connected to Reduck to run reduck/x.com/create_list, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/x.com/create_list

### Is there a x.com API to create X List?

You do not need one. "Create X List" drives the real x.com pages in a browser, so it works whether or not x.com offers an API for this.

### What information do I need to provide?

Required: name. Optional: private, description.

### What does it return?

It returns url, name, list_id, private, description.

### Do I need to be logged in to x.com?

Yes. It acts as you on x.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the x.com cookies saved by the Reduck extension.

### Does it change anything on x.com, or only read data?

It makes changes on x.com, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/x.com/create_list, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/x.com/create_list

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/x.com/create_list
