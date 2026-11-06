# List my n8n Creator Portal templates

Automatically list my n8n Creator Portal templates on creators.n8n.io. List the workflow templates the signed-in creator has submitted on the n8n Creator Portal (creators.n8n.io), whatever their state, as the portal gives them. Returns per template its id, name, review status (ai_review, in_review, changes_needed, published or wont_publish), view count, dates, and the AI review once it has answered (its decision, its feedback text and the title it suggests; null before). A creator with no template gets an empty list. Pass an id to creators.n8n.io/get_my_template for the description, the workflow, the price and the purchase link.

- Site: creators.n8n.io
- Address: `reduck/creators.n8n.io/list_my_templates`
- Updated: 2026-11-05 (v6)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/creators.n8n.io/list_my_templates`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/creators.n8n.io/list_my_templates
```

## Input

It takes no input.

## Output

- `templates` (array, required): Every template of the signed-in creator, as the portal's API sends it. Fields the API adds later are passed through.

## FAQ

### What does "List my n8n Creator Portal templates" do?

List the workflow templates the signed-in creator has submitted on the n8n Creator Portal (creators.n8n.io), whatever their state, as the portal gives them. Returns per template its id, name, review status (ai_review, in_review, changes_needed, published or wont_publish), view count, dates, and the AI review once it has answered (its decision, its feedback text and the title it suggests; null before). A creator with no template gets an empty list. Pass an id to creators.n8n.io/get_my_template for the description, the workflow, the price and the purchase link.

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
