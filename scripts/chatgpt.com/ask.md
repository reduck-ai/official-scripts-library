# Ask ChatGPT

Automatically ask ChatGPT on chatgpt.com. See what ChatGPT tells a stranger about your market and which pages it cites to back that up.

- Site: chatgpt.com
- Address: `reduck/chatgpt.com/ask`
- Updated: 2026-10-05 (v39)
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
- `mode` (string, optional): Signed in, which ChatGPT application answers: chat, or work (Work mode, with its own models and larger search result lists). The choice is saved on the account, so it holds for later chats too. Omitted: whichever the account used last; `mode` in the result says which.

## Output

- `mode` (string | null, required): The ChatGPT application that answered: chat, or work (Work mode), as the saved conversation records it. Null signed out, where the page offers no choice.
- `calls` (array, required): One entry per search call, as the page numbers them. A call often runs a whole round of queries at once (measured 2026-09-23: 9 queries in 2 calls) and answers one list for all of them. What the page does not receive: which query returned which result, the call's arguments, and which search backend answered it. Empty when it did not search, and signed out.
- `model` (string | null, required): Which model answered, by ChatGPT's own id (e.g. "gpt-5-6"). Null when the app does not say.
- `answer` (string | null, required): The answer as markdown, as ChatGPT's own Copy gives it: each citation is a markdown link to its source. Null signed out: `answers` has its text there.
- `answers` (array, required): One entry per assistant turn, as rendered. Usually one; ChatGPT sometimes serves a paired-response variant that answers twice and asks which reply you prefer, and neither entry is more official than the other — read the length before reading answers[0]. Inline citation chips appear as their publisher's name in the text, and mathematical notation linearizes lossily.
- `sources` (array, required): Every page the searches put in front of the model, once each, in the order it got them — the pool the answer could draw on, as opposed to `references`, what it cited. Empty signed out.
- `searches` (array, required): One entry per round of web searches, in order: what the model typed and the results put in front of it. Empty when it did not search, and signed out.
- `references` (array, required): Every source the answer CITED — not everything the search retrieved (that is `sources`) — deduplicated by url and in the order the answer surfaced them. Empty when the answer did not search, which is a fact about that reply rather than a failure: the same question searches on one run and not the next.
- `stopReason` (string | null, required): Why generation ended, as ChatGPT records it: "stop" for an answer the model finished. Null when ChatGPT records no reason: signed out, and in Work mode (`mode: "work"`), whose answers never carry one (measured 2026-09-25, 4 of 4 Work runs). Null is then not a cut-off answer; the script returns only once the answer has stopped growing. A finished answer can still be only a sentence announcing work it never did; that is what the model returned, not a truncation.
- `searchContext` (object, required): What the server says about this turn's search, as sent to the page. Signed in it is no longer sent (2026-09-26), so every field is null there. One of ChatGPT's two signed-out applications sends it; the other (the one that opens a /uc/ chat) does not. A field is also null when the app did not send it.
- `conversationId` (string | null, required): The conversation's id, from the /c/<id> or /uc/<id> URL. Null if the app did not navigate.
- `webSearchQueries` (array, required): The searches ChatGPT issued, in order. Signed in, read from the saved conversation. Signed out, one of ChatGPT's two applications names them on its answer stream; the one that opens a /uc/ chat does not, so the list is empty there even when `references` shows the reply searched. Empty also when the reply did not search.

## Example output

Shape only: placeholder values generated from the output schema, not a real run.

```json
{
  "mode": "chat",
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
      "url": "https://example.com/item/123",
      "title": "Example",
      "attribution": "…"
    }
  ],
  "stopReason": "…",
  "searchContext": {
    "tool": "…",
    "useCase": "…",
    "toolInvoked": true,
    "locationUsed": "…",
    "clusterRegion": "…",
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

Required: question. Optional: mode.

### What does it return?

It returns mode, calls, model, answer, answers, sources, searches, references, stopReason, searchContext, conversationId, webSearchQueries.

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
