# List Welcome to the Jungle email templates

Automatically list Welcome to the Jungle email templates on welcomekit.co. List the ATS organization's email templates. Returns templates (id, name, reference) for the org. id is the join key for send_template_email; reference is the built-in key (new, refused, interview, phone_call) or null for custom templates.

- Site: welcomekit.co
- Address: `reduck/welcomekit.co/list_email_templates`
- Updated: 2026-10-06 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/welcomekit.co/list_email_templates`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/welcomekit.co/list_email_templates
```

## Input

- `org` (string, required): Organization reference as it appears in your dashboard URL https://www.welcomekit.co/dashboard/o/<org>/ (6-char code).

## Output

- `org` (string, required)
- `templates` (array, required)

## FAQ

### What does "List Welcome to the Jungle email templates" do?

List the ATS organization's email templates. Returns templates (id, name, reference) for the org. id is the join key for send_template_email; reference is the built-in key (new, refused, interview, phone_call) or null for custom templates.

### How do I automatically list Welcome to the Jungle email templates on welcomekit.co?

Ask an AI agent connected to Reduck to run reduck/welcomekit.co/list_email_templates, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/welcomekit.co/list_email_templates

### Is there a welcomekit.co API to list Welcome to the Jungle email templates?

You do not need one. "List Welcome to the Jungle email templates" drives the real welcomekit.co pages in a browser, so it works whether or not welcomekit.co offers an API for this.

### What information do I need to provide?

Required: org.

### What does it return?

It returns org, templates.

### Do I need to be logged in to welcomekit.co?

Yes. It acts as you on welcomekit.co: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the welcomekit.co cookies saved by the Reduck extension.

### Does it change anything on welcomekit.co, or only read data?

It only reads. It looks things up on welcomekit.co and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/welcomekit.co/list_email_templates, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/welcomekit.co/list_email_templates

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/welcomekit.co/list_email_templates
