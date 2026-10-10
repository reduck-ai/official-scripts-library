# Get Welcome to the Jungle email templates (with body)

Automatically get Welcome to the Jungle email templates (with body) on welcomekit.co. Read the ATS organization's email templates with their full content (subject + body), not just id/name. Returns every template, or filter to one by id or name (case-insensitive). body/subject carry placeholders like [firstname], [job_name]. Use to inspect exactly what send_template_email will send before sending it.

- Site: welcomekit.co
- Address: `reduck/welcomekit.co/get_email_template`
- Updated: 2026-10-09 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/welcomekit.co/get_email_template`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/welcomekit.co/get_email_template
```

## Input

- `org` (string, required): Organization reference from your dashboard URL https://www.welcomekit.co/dashboard/o/<org>/ (6-char code).
- `id` (integer, optional): Optional: return only the template with this id (from list_email_templates).
- `name` (string, optional): Optional: return only templates whose name matches this (case-insensitive, exact). Ignored if id is set.

## Output

- `org` (string, required)
- `templates` (array, required)

## FAQ

### What does "Get Welcome to the Jungle email templates (with body)" do?

Read the ATS organization's email templates with their full content (subject + body), not just id/name. Returns every template, or filter to one by id or name (case-insensitive). body/subject carry placeholders like [firstname], [job_name]. Use to inspect exactly what send_template_email will send before sending it.

### How do I automatically get Welcome to the Jungle email templates (with body) on welcomekit.co?

Ask an AI agent connected to Reduck to run reduck/welcomekit.co/get_email_template, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/welcomekit.co/get_email_template

### Is there a welcomekit.co API to get Welcome to the Jungle email templates (with body)?

You do not need one. "Get Welcome to the Jungle email templates (with body)" drives the real welcomekit.co pages in a browser, so it works whether or not welcomekit.co offers an API for this.

### What information do I need to provide?

Required: org. Optional: id, name.

### What does it return?

It returns org, templates.

### Do I need to be logged in to welcomekit.co?

Yes. It acts as you on welcomekit.co: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the welcomekit.co cookies saved by the Reduck extension.

### Does it change anything on welcomekit.co, or only read data?

It only reads. It looks things up on welcomekit.co and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/welcomekit.co/get_email_template, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/welcomekit.co/get_email_template

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/welcomekit.co/get_email_template
