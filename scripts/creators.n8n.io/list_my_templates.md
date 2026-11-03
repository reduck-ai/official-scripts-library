# List my n8n Creator Portal templates

Automatically list my n8n Creator Portal templates on creators.n8n.io. List the workflow templates the signed-in creator has submitted on the n8n Creator Portal (creators.n8n.io), whatever their state. Returns per template its id, name, review status (ai_review: the AI check runs or its feedback waits for you to finalize; in_review: a person reviews it; changes_needed; published; wont_publish), price and purchase link (null for a free template), view count, dates, whether AI feedback is ready, and its n8n.io url once published. A creator with no template gets an empty list. Pass an id to creators.n8n.io/get_my_template for its description, AI feedback and workflow.

- Site: creators.n8n.io
- Address: `reduck/creators.n8n.io/list_my_templates`
- Updated: 2026-11-02 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/creators.n8n.io/list_my_templates`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/creators.n8n.io/list_my_templates
```

## Input

It takes no input.

## Output

- `templates` (array, required)

## FAQ

### What does "List my n8n Creator Portal templates" do?

List the workflow templates the signed-in creator has submitted on the n8n Creator Portal (creators.n8n.io), whatever their state. Returns per template its id, name, review status (ai_review: the AI check runs or its feedback waits for you to finalize; in_review: a person reviews it; changes_needed; published; wont_publish), price and purchase link (null for a free template), view count, dates, whether AI feedback is ready, and its n8n.io url once published. A creator with no template gets an empty list. Pass an id to creators.n8n.io/get_my_template for its description, AI feedback and workflow.

### How do I automatically list my n8n Creator Portal templates on creators.n8n.io?

Ask an AI agent connected to Reduck to run reduck/creators.n8n.io/list_my_templates, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/creators.n8n.io/list_my_templates

### Is there a creators.n8n.io API to list my n8n Creator Portal templates?

You do not need one. "List my n8n Creator Portal templates" drives the real creators.n8n.io pages in a browser, so it works whether or not creators.n8n.io offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns templates.

### Do I need to be logged in to creators.n8n.io?

Yes. It acts as you on creators.n8n.io: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the creators.n8n.io cookies saved by the Reduck extension.

### Does it change anything on creators.n8n.io, or only read data?

It only reads. It looks things up on creators.n8n.io and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/creators.n8n.io/list_my_templates, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/creators.n8n.io/list_my_templates

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/creators.n8n.io/list_my_templates
