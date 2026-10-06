# Ask Perplexity

Automatically ask Perplexity on perplexity.ai. Ask a question, get the answer plus every page the search pulled and the ones it cited.

- Site: perplexity.ai
- Address: `reduck/perplexity.ai/ask`
- Updated: 2026-10-05 (v14)
- Author: Reduck AI (reduck)

## About

Say you run marketing for a bike light brand and Perplexity keeps recommending someone else's. Ask "best rear light for commuting in the rain" and the answer is the least useful part of what comes back. Sources is everything the search pulled, while citations is the shorter list that got a chip in the text, with trustedDomain set on the ones Perplexity marks as trusted. Run the question five times and tally the domains in both lists, because answers shift between runs. If your product page sits in sources but never earns a chip, open threadUrl before you blame the page: a chip like "bikeradar +2" credits two more pages that only appear in sources. If you are in neither list, note which review sites keep getting chips. Each run starts a new thread, so it stays in your Perplexity history.

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

## Example output

Shape only: placeholder values generated from the output schema, not a real run.

```json
{
  "answer": "…",
  "sources": [
    {
      "url": "https://example.com/item/123",
      "title": "Example",
      "snippet": "…",
      "publisher": "…"
    }
  ],
  "question": "…",
  "citations": [
    {
      "url": "https://example.com/item/123",
      "label": "Example",
      "trustedDomain": true
    }
  ],
  "threadUrl": "https://example.com/item/123",
  "answerChars": 3,
  "researchSteps": [
    "…"
  ]
}
```

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

It makes changes on perplexity.ai, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/perplexity.ai/ask, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/perplexity.ai/ask

### Who maintains it?

It is part of Reduck's official curated catalogue.

### Can I see the actual search queries Perplexity ran?

No. Perplexity does not show its raw search queries anywhere on a thread, so they cannot be returned. researchSteps holds its plain-language plan instead, one line per step, written in the interface language. Source titles also arrive cut off with an ellipsis, the same way the Links view shows them.

### Can I pick Pro Search, Research mode or a specific model?

No. The only input is the question, which is typed into the composer and submitted, so the run uses whatever mode and model the composer is set to for that account. An answer still being written after about two minutes ends the run with an error.

### Can I ask a follow-up in the same thread?

No. Every run opens a new thread from a single question. The threadUrl in the result points to it, so you can open it in Perplexity and continue by hand.

### Why does a run fail with a sign-up message instead of an answer?

Perplexity can gate asks once a free-tier rate limit is spent, and that gate has fired even on a signed-in free account. The run stops with an error naming the limit instead of returning an empty answer. Retrying later or using a paid plan are the known ways past it.

Source: https://reduck.ai/explore/scripts/reduck/perplexity.ai/ask
