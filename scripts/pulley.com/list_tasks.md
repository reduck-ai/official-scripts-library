# Pulley — list my tasks

Automatically list my tasks on pulley.com. List the signed-in Pulley user's pending tasks across all companies (e.g. sign a document, accept a grant, exercise options): each task's type, object id, name, company, date, document type, shares, security class and equity plan. Read-only; signed out is a clear error. A user with nothing pending returns an empty list — only that case has been observed so far.

- Site: pulley.com
- Address: `reduck/pulley.com/list_tasks`
- Updated: 2026-09-28 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/pulley.com/list_tasks`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/pulley.com/list_tasks
```

## Input

It takes no input.

## Output

- `count` (integer, required)
- `tasks` (array, required)

## FAQ

### What does "Pulley — list my tasks" do?

List the signed-in Pulley user's pending tasks across all companies (e.g. sign a document, accept a grant, exercise options): each task's type, object id, name, company, date, document type, shares, security class and equity plan. Read-only; signed out is a clear error. A user with nothing pending returns an empty list — only that case has been observed so far.

### How do I automatically list my tasks on pulley.com?

Ask an AI agent connected to Reduck to run reduck/pulley.com/list_tasks, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/pulley.com/list_tasks

### Is there a pulley.com API to list my tasks?

You do not need one. "Pulley — list my tasks" drives the real pulley.com pages in a browser, so it works whether or not pulley.com offers an API for this.

### What information do I need to provide?

Nothing. It takes no input.

### What does it return?

It returns count, tasks.

### Do I need to be logged in to pulley.com?

Yes. It acts as you on pulley.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the pulley.com cookies saved by the Reduck extension.

### Does it change anything on pulley.com, or only read data?

It only reads. It looks things up on pulley.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/pulley.com/list_tasks, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/pulley.com/list_tasks

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/pulley.com/list_tasks
