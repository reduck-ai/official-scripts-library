# Get one of my n8n Creator Portal templates

Automatically get one of my n8n Creator Portal templates on creators.n8n.io. Read one workflow template the signed-in creator submitted on the n8n Creator Portal (creators.n8n.io), by its id: name, review status, price and purchase link, dates, its description (Markdown, in the portal's sections: Quick overview, How it works, Setup, Requirements, Customization, Additional info), the workflow JSON as submitted, and the AI review's feedback once it is ready (its score explanation and the workflow JSON it suggests, null before). An id that is not one of the creator's templates fails with a clear message: get ids from creators.n8n.io/list_my_templates.

- Site: creators.n8n.io
- Address: `reduck/creators.n8n.io/get_my_template`
- Updated: 2026-11-02 (v1)
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
- `name` (string | null, required)
- `reviewStatus` (string | null, required)
- `url` (string | null, optional)
- `price` (number | null, optional)
- `views` (integer | null, optional)
- `workflow` (object | null, optional): The submitted workflow JSON (nodes, connections).
- `createdAt` (string | null, optional)
- `updatedAt` (string | null, optional)
- `aiFeedback` (object | null, optional): The AI review's answer as the portal gives it, e.g. workflowScoreExplanation and suggestedJson. Null until it is ready.
- `description` (string | null, optional): Markdown, in ## sections.
- `publishedAt` (string | integer | null, optional)
- `purchaseUrl` (string | null, optional)
- `hasAiFeedback` (boolean, optional)

## FAQ

### What does "Get one of my n8n Creator Portal templates" do?

Read one workflow template the signed-in creator submitted on the n8n Creator Portal (creators.n8n.io), by its id: name, review status, price and purchase link, dates, its description (Markdown, in the portal's sections: Quick overview, How it works, Setup, Requirements, Customization, Additional info), the workflow JSON as submitted, and the AI review's feedback once it is ready (its score explanation and the workflow JSON it suggests, null before). An id that is not one of the creator's templates fails with a clear message: get ids from creators.n8n.io/list_my_templates.

### How do I automatically get one of my n8n Creator Portal templates on creators.n8n.io?

Ask an AI agent connected to Reduck to run reduck/creators.n8n.io/get_my_template, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/creators.n8n.io/get_my_template

### Is there a creators.n8n.io API to get one of my n8n Creator Portal templates?

You do not need one. "Get one of my n8n Creator Portal templates" drives the real creators.n8n.io pages in a browser, so it works whether or not creators.n8n.io offers an API for this.

### What information do I need to provide?

Required: id.

### What does it return?

It returns id, url, name, price, views, workflow, createdAt, updatedAt, aiFeedback, description, publishedAt, purchaseUrl, reviewStatus, hasAiFeedback.

### Do I need to be logged in to creators.n8n.io?

Yes. It acts as you on creators.n8n.io: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the creators.n8n.io cookies saved by the Reduck extension.

### Does it change anything on creators.n8n.io, or only read data?

It only reads. It looks things up on creators.n8n.io and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/creators.n8n.io/get_my_template, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/creators.n8n.io/get_my_template

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/creators.n8n.io/get_my_template
