# Ask Muse (muse.ai)

Automatically ask Muse (muse.ai) on muse.ai. Open a new side chat with Muse, Meta's personal agent at muse.ai, send one question, wait until Muse ends its reply (up to about 3 minutes), and return what Muse posted: the answer as markdown, each message and widget of the turn, and the web pages it used as sources.

- Site: muse.ai
- Address: `reduck/muse.ai/ask`
- Updated: 2026-11-27 (v5)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/muse.ai/ask`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/muse.ai/ask
```

## Input

- `question` (string, required): The question to send as the first message of a new side chat. Line breaks are kept. It must hold at least one character that is not a space.

## Output

- `url` (string, required): Address of the side chat on muse.ai: https://muse.ai/thread/<threadId>. Muse posts the result of work still pending there.
- `answer` (string, required): The markdown of every reply message of the turn, in order, separated by a blank line. Links keep their real address.
- `askedAt` (string | null, required): When Muse's server recorded the question (ISO 8601). With the createdAt of Muse's last completed message, here or in muse.ai/get_chat once pending work ends, it gives how long Muse took. Null when Muse gave no time.
- `pending` (boolean | null, required): True when Muse is still working on the question as the run returns (its activity for this chat is still open): the answer is then its first reply, and Muse posts its result later at url. False when the work is done or used no tool. Null when the browser hides Muse's activity panel, so the run cannot tell.
- `sources` (array, required): Every source of the turn's messages, deduplicated by url, in order of first appearance.
- `messages` (array, required): What Muse posted in reply to the question when the run returned, in order.
- `threadId` (string, required): Id of the new side chat.

## FAQ

### What does "Ask Muse (muse.ai)" do?

Open a new side chat with Muse, Meta's personal agent at muse.ai, send one question, wait until Muse ends its reply (up to about 3 minutes), and return what Muse posted: the answer as markdown, each message and widget of the turn, and the web pages it used as sources.

### How do I automatically ask Muse (muse.ai) on muse.ai?

Ask an AI agent connected to Reduck to run reduck/muse.ai/ask, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/muse.ai/ask

### Is there a muse.ai API to ask Muse (muse.ai)?

You do not need one. "Ask Muse (muse.ai)" drives the real muse.ai pages in a browser, so it works whether or not muse.ai offers an API for this.

### What information do I need to provide?

Required: question.

### What does it return?

It returns url, answer, askedAt, pending, sources, messages, threadId.

### Do I need to be logged in to muse.ai?

Yes. It acts as you on muse.ai: in your browser it reuses your session, and on a cloud browser it loads your Auth session cookies for muse.ai.

### Does it change anything on muse.ai, or only read data?

It makes changes on muse.ai, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/muse.ai/ask, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/muse.ai/ask

### Who maintains it?

It is one of Reduck's official scripts.

Source: https://reduck.ai/explore/scripts/reduck/muse.ai/ask
