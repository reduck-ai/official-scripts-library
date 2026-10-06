# Search Perplexity chats

Automatically search Perplexity chats on perplexity.ai. Type a topic you remember and get back the matching threads, each with a snippet and an ID to open it.

- Site: perplexity.ai
- Address: `reduck/perplexity.ai/search_chats`
- Updated: 2026-10-05 (v1)
- Author: Reduck AI (reduck)

## About

Perplexity builds each thread's title from your first question, so months later the thread you want sits under wording you forgot, or its useful answer came four follow-ups in. The Library page has a search icon for this, and Perplexity said in February 2026 that past-thread search no longer needs exact keywords and can land on an answer inside a follow-up. None of its developer APIs touch your own history, and search_chats runs that same Library search in your signed-in browser. Each hit returns its title, Perplexity's snippet, the last update and a chatId. Say a consultant spent last spring on EU battery passport rules. Searching battery passport turns up four threads, and the newest one's chatId goes to get_chat_messages for the questions and answers behind a client memo. Source links stay behind, so the citations mean reopening the thread. Only the first page of results comes back, so a rare word beats a broad one like regulation.

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/perplexity.ai/search_chats`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/perplexity.ai/search_chats
```

## Input

- `query` (string, required): Search term, matched against thread titles and answer text.

## Output

- `chats` (array, required)
- `query` (string, required)
- `hasMore` (boolean, required): Whether more matching threads exist beyond the ones returned here.

## Example output

Shape only: placeholder values generated from the output schema, not a real run.

```json
{
  "chats": [
    {
      "mode": "…",
      "title": "Example",
      "chatId": "abc123",
      "status": "…",
      "isUnread": true,
      "contextId": "abc123",
      "updatedAt": "2026-01-15T09:30:00Z",
      "searchPreview": "…"
    }
  ],
  "query": "…",
  "hasMore": true
}
```

## FAQ

### What does "Search Perplexity chats" do?

Search your Perplexity thread history by keyword, via the Sessions library's search box.

### How do I automatically search Perplexity chats on perplexity.ai?

Ask an AI agent connected to Reduck to run reduck/perplexity.ai/search_chats, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/perplexity.ai/search_chats

### Is there a perplexity.ai API to search Perplexity chats?

You do not need one. "Search Perplexity chats" drives the real perplexity.ai pages in a browser, so it works whether or not perplexity.ai offers an API for this.

### What information do I need to provide?

Required: query.

### What does it return?

It returns chats, query, hasMore.

### Do I need to be logged in to perplexity.ai?

Yes. It acts as you on perplexity.ai: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the perplexity.ai cookies saved by the Reduck extension.

### Does it change anything on perplexity.ai, or only read data?

It only reads. It looks things up on perplexity.ai and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/perplexity.ai/search_chats, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/perplexity.ai/search_chats

### Who maintains it?

It is part of Reduck's official curated catalogue.

### Does search_chats return every Perplexity thread that matches?

The search_chats script returns only the first page of results that Perplexity's Library search sends back, with hasMore set to true when more matches exist and no page or cursor input to go further. Perplexity, not the script, decides how many threads fit on that page, so when hasMore is true, search again with a rarer word such as a client, product or company name.

### How do I list my recent Perplexity threads without searching?

The list_chats script takes no input and returns the threads in your Perplexity sidebar, newest first, each with a preview of its answer. search_chats goes through the Library search instead, so it can reach threads that have dropped out of the sidebar, and it shows the snippet Perplexity picked for the match. Both return the same chatId, which get_chat_messages takes to fetch a thread's questions and answers.

### Can I delete an old Perplexity thread that search_chats found?

Only when the thread still shows in your recent Perplexity sidebar. The delete_chat script looks for it there and stops with an error once it has dropped off that list, so an older thread found through search cannot be deleted this way, although get_chat_messages can still read it.

### Can I search my Perplexity history for an exact phrase in quotation marks?

Leave double quotation marks and backslashes out of the search term: with either one in it, search_chats never gets its results back and the run fails after about 15 seconds. Perplexity says exact keyword matches are not needed when searching past threads, so a few plain words from the thread are the better bet.

Source: https://reduck.ai/explore/scripts/reduck/perplexity.ai/search_chats
