# Ask Perplexity

Automatically ask Perplexity on perplexity.ai. Ask Perplexity a question and get back three things the answer alone cannot tell you apart: the answer itself, the research steps Perplexity says it took to write it, and every page its search returned — not only the ones the answer cited.

- Site: perplexity.ai
- Address: `reduck/perplexity.ai/ask`
- Updated: 2026-09-11 (v13)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/perplexity.ai/ask`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/perplexity.ai/ask
```

## Input

- `question` (string, required): The question to ask, sent as the first message of a new thread.

## Output

- `answer` (string, required): The answer as rendered, with its paragraphs, lists and tables flattened to text in reading order. Inline citation chips read as the publisher name Perplexity shows, e.g. 'coursera +2'.
- `sources` (array, required): Every page the search returned, cited or not - the candidate pool, in the order the Links view lists it. `sources` minus `citations` is what Perplexity retrieved and then passed over; a URL in neither was never retrieved. Empty when the answer searched nothing.
- `question` (string, required)
- `citations` (array, required): The sources cited inline by the answer, in the order they appear, deduplicated by URL. A subset of `sources` whenever the answer searched.
- `threadUrl` (string | null, required): URL of the thread the answer was written into, so the run can be audited afterwards.
- `answerChars` (integer, required)
- `researchSteps` (array, required): Perplexity's own description of each step of its research plan, in order, e.g. 'Searching for fermentation differences'. These are written for the reader in the interface language, not the raw queries the search issued - Perplexity does not expose those. Empty when the answer was written without a research plan.

## FAQ

### What does "Ask Perplexity" do?

Ask Perplexity a question and get back three things the answer alone cannot tell you apart: the answer itself, the research steps Perplexity says it took to write it, and every page its search returned — not only the ones the answer cited.

### How do I automatically ask Perplexity on perplexity.ai?

Ask an AI agent connected to Reduck to run reduck/perplexity.ai/ask, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/perplexity.ai/ask

### Is there a perplexity.ai API to ask Perplexity?

You do not need one. "Ask Perplexity" drives the real perplexity.ai pages in a browser, so it works whether or not perplexity.ai offers an API for this.

### What information do I need to provide?

Required: question.

### What does it return?

It returns answer, sources, question, citations, threadUrl, answerChars, researchSteps.

### Do I need to be logged in to perplexity.ai?

Yes. It acts as you on perplexity.ai: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the perplexity.ai cookies saved by the Reduck extension.

### Does it change anything on perplexity.ai, or only read data?

It makes changes on perplexity.ai, like sending, posting or booking something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/perplexity.ai/ask, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/perplexity.ai/ask

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/perplexity.ai/ask
