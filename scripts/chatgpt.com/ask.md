# Ask ChatGPT

Automatically ask ChatGPT on chatgpt.com. See what ChatGPT tells a stranger about your market and which pages it cites to back that up.

- Site: chatgpt.com
- Address: `reduck/chatgpt.com/ask`
- Updated: 2026-10-20 (v54)
- Author: Reduck AI (reduck)

## About

A growth lead at a French payroll startup sends "What payroll software should a 20-person company in France use?" from a signed-out browser every Monday and logs which vendors the reply names and which review sites it cites, since those are the pages worth getting listed on. Signed out is the closest thing to a stranger asking, but you get little beyond the reply text and its cited references. A signed-in account adds the model id, every query ChatGPT typed and every page those searches pulled up, though saved memory can shape the reply and the chat is kept in that account's history. Those queries are worth a close read, since one question can fan out into many (a September run typed 9 across 2 search calls). Each run is one question in a fresh chat, and setting mode to work is saved on the account, so your own next chat starts in Work too.

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/chatgpt.com/ask`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/chatgpt.com/ask
```

## Input

- `question` (string, required): The question to send as the first message of a new chat.

## Output

- `calls` (array | null, required): One entry per search call. A call often runs a whole round of queries at once and answers one list for all of them. What the page does not receive: which query returned which result, the call's arguments, and which search backend answered it. Empty when it did not search. Null signed out, where ChatGPT does not show them.
- `model` (string | null, required): Which model answered, by ChatGPT's own id (e.g. "gpt-6"). Null when the app does not say, which is always the case signed out.
- `answer` (string, required): The last entry of `answers`.
- `answers` (array, required): One entry per reply, usually one; ChatGPT sometimes answers twice and asks which reply you prefer, and neither entry is more official than the other: read the length before reading answers[0]. Each is the reply as markdown, each citation a markdown link to its source, widgets (images, forms) left out.
- `sources` (array | null, required): Every page the searches put in front of the model, once each, in the order it got them: the pool the answer could draw on, as opposed to `references`, what it cited. Empty when it did not search. Null signed out, where ChatGPT does not show them.
- `activity` (array, required): The progress lines ChatGPT showed while it worked, in order and in the display language, e.g. "Searching the web", "Searched 8 websites". Signed out, the only trace of the searches it ran. Display text: its wording and its counts are ChatGPT's, not a count of `sources`. Empty when it showed none.
- `searches` (array | null, required): One entry per round of web searches, in order: what the model typed and the results put in front of it. Empty when it did not search. Null signed out, where ChatGPT does not show them.
- `references` (array, required): Every source the answer cited or linked, signed in or out, deduplicated by url and in the order the answer surfaced them. Not everything the searches retrieved: that is `sources`. Empty when the answer cited nothing, which is a fact about that reply: the same question searches on one run and not the next.
- `stopReason` (string | null, required): Why generation ended, as ChatGPT records it: "stop" for an answer the model finished. Null when ChatGPT records no reason, and signed out. A finished answer can still be only a sentence announcing work it never did; that is what the model returned, not a truncation.
- `searchContext` (object, required): What the app asked for and what the server says about this turn, as sent to the page. Signed out, every field the server sends is null, and a field is null when the app did not send it.
- `conversationId` (string | null, required): The conversation's id. Null if the app did not create one.
- `webSearchQueries` (array | null, required): The searches ChatGPT issued, in order. Empty when the reply did not search. Null signed out, where ChatGPT does not show them: unknown, not none.

## Example output

Shape only: placeholder values generated from the output schema, not a real run.

```json
{
  "calls": [
    {
      "call": 3,
      "tool": "…",
      "results": [
        {
          "ref": "…",
          "url": "https://example.com/item/123",
          "rank": 3,
          "type": "…",
          "title": "Example",
          "pubDate": "2026-01-15T09:30:00Z",
          "snippet": "…",
          "attribution": "…",
          "thumbnailUrl": "https://example.com/item/123"
        }
      ]
    }
  ],
  "model": "…",
  "answer": "…",
  "answers": [
    "…"
  ],
  "sources": [
    {
      "url": "https://example.com/item/123",
      "title": "Example",
      "attribution": "…"
    }
  ],
  "activity": [
    "…"
  ],
  "searches": [
    {
      "queries": [
        "…"
      ],
      "results": [
        {
          "ref": "…",
          "url": "https://example.com/item/123",
          "type": "…",
          "title": "Example",
          "pubDate": "2026-01-15T09:30:00Z",
          "attribution": "…"
        }
      ]
    }
  ],
  "references": [
    {
      "ref": "…",
      "url": "https://example.com/item/123",
      "title": "Example",
      "attribution": "…"
    }
  ],
  "stopReason": "…",
  "searchContext": {
    "tool": "…",
    "useCase": "…",
    "planType": "…",
    "toolInvoked": true,
    "locationUsed": "…",
    "clusterRegion": "…",
    "requestedModel": "…",
    "thinkingEffort": "…",
    "modelExperience": "…",
    "locationIsPrecise": true
  },
  "conversationId": "abc123",
  "webSearchQueries": [
    "…"
  ]
}
```

## FAQ

### What does "Ask ChatGPT" do?

Open a new ChatGPT chat, send one question, wait for the answer to finish (up to 3 minutes), and return the answer, the sources it cited, and the web searches it ran.

### How do I automatically ask ChatGPT on chatgpt.com?

Ask an AI agent connected to Reduck to run reduck/chatgpt.com/ask, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/chatgpt.com/ask

### Is there a chatgpt.com API to ask ChatGPT?

You do not need one. "Ask ChatGPT" drives the real chatgpt.com pages in a browser, so it works whether or not chatgpt.com offers an API for this.

### What information do I need to provide?

Required: question.

### What does it return?

It returns calls, model, answer, answers, sources, activity, searches, references, stopReason, searchContext, conversationId, webSearchQueries.

### Do I need to be logged in to chatgpt.com?

No. It only uses pages of chatgpt.com that are reachable without signing in.

### Does it change anything on chatgpt.com, or only read data?

It makes changes on chatgpt.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/chatgpt.com/ask, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/chatgpt.com/ask

### Who maintains it?

It is part of Reduck's official curated catalogue.

### Why does ChatGPT cite different sources each time I ask the same question?

ChatGPT decides on each reply whether to search the web, so one run can cite several pages and the next none at all. When it does search, the queries it types can change between runs, and the pages it reads and cites shift with them. An empty references list means that reply skipped the search, not that the run failed.

### Does the OpenAI API return the same answer a ChatGPT user sees?

No. OpenAI describes each API request as independent and stateless, so the reply comes from the model and the messages you send, without the history or saved memory a ChatGPT account brings to the app. API usage is billed apart from any ChatGPT plan, and the standard web search tool costs $10 per 1,000 calls plus the retrieved content billed as tokens at the model's rate.

### Can I run a batch of ChatGPT questions at the same time from one account?

You can, but spread them out. When several runs share one signed-in account at the same moment, ChatGPT has been seen sending tabs back to the home page mid-answer, and Reduck's Ask ChatGPT script reopens the chat up to two times, then stops with an error. If ChatGPT refuses a message (a rate limit or a moderation block), the run ends at once with ChatGPT's own error text instead of waiting out its three-minute budget.

### Does ChatGPT answer differently depending on the country I ask from?

It can. OpenAI says ChatGPT search estimates a general location (country, state or city) from your IP address and that a VPN can change that guess, so the same question asked from Paris and from Brussels may come back different. Signed-out replies sometimes report the place in searchContext.locationUsed, and to track one market the sensible habit is to run from a browser in that market and keep it there.

Source: https://reduck.ai/explore/scripts/reduck/chatgpt.com/ask
