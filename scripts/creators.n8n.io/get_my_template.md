# Get one of my n8n Creator Portal templates

Automatically get one of my n8n Creator Portal templates on creators.n8n.io. Read one workflow template the signed-in creator submitted on the n8n Creator Portal (creators.n8n.io), by its id, as the portal gives it: name, review status (ai_review, in_review, changes_needed, published or wont_publish), price and purchase link (null for a free template), view count, dates, its description (Markdown, in the portal's sections: Quick overview, How it works, Setup, Requirements, Customization, Additional info), the workflow as submitted with the portal's count of its nodes, and the AI review once it has answered (its decision, scores with their explanations, feedback text, and the title, description and workflow it suggests; null before). An id that is not one of the creator's templates fails with a clear message: get ids from creators.n8n.io/list_my_templates.

- Site: creators.n8n.io
- Address: `reduck/creators.n8n.io/get_my_template`
- Updated: 2026-11-05 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/creators.n8n.io/get_my_template`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/creators.n8n.io/get_my_template
```

## Input

- `id` (integer, required): The template's id, from creators.n8n.io/list_my_templates.

## Output

- `id` (integer, required)
- `reviewStatus` (string | null, required): Where the template is in the portal's review: ai_review, in_review, changes_needed, published or wont_publish.
- `name` (string | null, optional): "New Submission" until the submission is finalized.
- `price` (number | null, optional): Null for a free template.
- `views` (integer | null, optional)
- `hidden` (boolean | null, optional)
- `status` (string | null, optional): The status as the API sends it next to reviewStatus.
- `quality` (any, optional): The quality mark as the API sends it, null when it has none.
- `username` (string | null, optional): The creator's n8n username.
- `workflow` (object | null, optional): The submitted workflow (name, nodes, connections, settings).
- `createdAt` (string | null, optional)
- `updatedAt` (string | null, optional)
- `aiFeedback` (object | null, optional): The AI review, null before it answers: aiDecision, the feedback text (feedbackHtml, in Markdown), scores with their explanations (general, workflow, description, title, security), and the title, description and workflow it suggests (suggestedTitle, suggestedDescription, suggestedJson), each null when it gives none.
- `description` (string | null, optional): Markdown, in the portal's ## sections.
- `purchaseUrl` (string | null, optional): Null for a free template.
- `workflowInfo` (object | null, optional): The portal's summary of the workflow: nodeCount, and nodeTypes with a count per node type.
- `publishedAtTimestamp` (string | null, optional): As the API sends it. It can be set on a template that is not published: read reviewStatus for the state.

## FAQ

### What does "Get one of my n8n Creator Portal templates" do?

Read one workflow template the signed-in creator submitted on the n8n Creator Portal (creators.n8n.io), by its id, as the portal gives it: name, review status (ai_review, in_review, changes_needed, published or wont_publish), price and purchase link (null for a free template), view count, dates, its description (Markdown, in the portal's sections: Quick overview, How it works, Setup, Requirements, Customization, Additional info), the workflow as submitted with the portal's count of its nodes, and the AI review once it has answered (its decision, scores with their explanations, feedback text, and the title, description and workflow it suggests; null before). An id that is not one of the creator's templates fails with a clear message: get ids from creators.n8n.io/list_my_templates.

### How do I automatically get one of my n8n Creator Portal templates on creators.n8n.io?

Ask an AI agent connected to Reduck to run reduck/creators.n8n.io/get_my_template, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/creators.n8n.io/get_my_template

### Is there a creators.n8n.io API to get one of my n8n Creator Portal templates?

You do not need one. "Get one of my n8n Creator Portal templates" drives the real creators.n8n.io pages in a browser, so it works whether or not creators.n8n.io offers an API for this.

### What information do I need to provide?

Required: id.

### What does it return?

It returns id, name, price, views, hidden, status, quality, username, workflow, createdAt, updatedAt, aiFeedback, description, purchaseUrl, reviewStatus, workflowInfo, publishedAtTimestamp.

### Do I need to be logged in to creators.n8n.io?

Yes. It acts as you on creators.n8n.io: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the creators.n8n.io cookies saved by the Reduck extension.

### Does it change anything on creators.n8n.io, or only read data?

It only reads. It looks things up on creators.n8n.io and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/creators.n8n.io/get_my_template, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/creators.n8n.io/get_my_template

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/creators.n8n.io/get_my_template
