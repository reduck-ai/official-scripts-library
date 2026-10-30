# Ask Google AI Mode

Automatically ask Google AI Mode on google.com. Ask Google AI Mode one question and wait for its answer (up to 2 min). Returns the answer as Markdown (headings, lists, tables and links kept) and the pages it cites, in the order the answer first cites them, each with url, title, site, byline and snippet; sources is empty when the answer cites nothing. Signed in to Google, the question is kept in the account's AI Mode history. One run is one draw: the same question can be answered or cited differently on the next run, and the answer follows the browser's account and location. A browser where Google offers no AI Mode fails with a message that says so.

- Site: google.com
- Address: `reduck/google.com/ask_ai_mode`
- Updated: 2026-10-29 (v2)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/google.com/ask_ai_mode`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/google.com/ask_ai_mode
```

## Input

- `question` (string, required): The question, as typed in AI Mode, e.g. 'best tools to monitor reddit mentions'.

## Output

- `text` (string, required): The answer as Markdown. Each citation chip is kept in its place as links to the pages it stands for, e.g. "([Reddit](https://…), [YouTube](https://…))".
- `sources` (array, required): The pages the answer cites, one per page, in the order the answer first cites them.

## FAQ

### What does "Ask Google AI Mode" do?

Ask Google AI Mode one question and wait for its answer (up to 2 min). Returns the answer as Markdown (headings, lists, tables and links kept) and the pages it cites, in the order the answer first cites them, each with url, title, site, byline and snippet; sources is empty when the answer cites nothing. Signed in to Google, the question is kept in the account's AI Mode history. One run is one draw: the same question can be answered or cited differently on the next run, and the answer follows the browser's account and location. A browser where Google offers no AI Mode fails with a message that says so.

### How do I automatically ask Google AI Mode on google.com?

Ask an AI agent connected to Reduck to run reduck/google.com/ask_ai_mode, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/google.com/ask_ai_mode

### Is there a google.com API to ask Google AI Mode?

You do not need one. "Ask Google AI Mode" drives the real google.com pages in a browser, so it works whether or not google.com offers an API for this.

### What information do I need to provide?

Required: question.

### What does it return?

It returns text, sources.

### Do I need to be logged in to google.com?

No. It only uses pages of google.com that are reachable without signing in.

### Does it change anything on google.com, or only read data?

It makes changes on google.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/google.com/ask_ai_mode, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/google.com/ask_ai_mode

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/google.com/ask_ai_mode
