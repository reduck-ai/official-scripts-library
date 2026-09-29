# Hugging Face — get a model, dataset or Space

Automatically get a model, dataset or Space on huggingface.co. Get one Hugging Face model, dataset or Space by id (e.g. "google/gemma-2b"): URL, author, commit sha, private / gated / disabled flags, likes, downloads, pipeline tag, library, license, tags, Space SDK and runtime stage, the full file list, and created / last-modified dates. Public repos need no sign-in; when signed in, the account's own private repos resolve too. An unknown or inaccessible repo is a clear error.

- Site: huggingface.co
- Address: `reduck/huggingface.co/get_repo`
- Updated: 2026-09-28 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/huggingface.co/get_repo`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/huggingface.co/get_repo
```

## Input

- `id` (string, required): Repo id, e.g. "google/gemma-2b" (from huggingface.co/list_user_repos or the repo URL).
- `type` (string, optional): Repo type (default model).

## Output

- `id` (string, required)
- `url` (string, required)
- `type` (string, required)
- `sdk` (string | null, optional)
- `sha` (string | null, optional)
- `tags` (array, optional)
- `files` (array, optional)
- `gated` (string | boolean | null, optional)
- `likes` (integer | null, optional)
- `author` (string | null, optional)
- `license` (string | null, optional)
- `private` (boolean | null, optional)
- `disabled` (boolean | null, optional)
- `createdAt` (string | null, optional)
- `downloads` (integer | null, optional)
- `libraryName` (string | null, optional)
- `pipelineTag` (string | null, optional)
- `lastModified` (string | null, optional)
- `runtimeStage` (string | null, optional): Spaces only: RUNNING, SLEEPING, BUILDING…

## FAQ

### What does "Hugging Face — get a model, dataset or Space" do?

Get one Hugging Face model, dataset or Space by id (e.g. "google/gemma-2b"): URL, author, commit sha, private / gated / disabled flags, likes, downloads, pipeline tag, library, license, tags, Space SDK and runtime stage, the full file list, and created / last-modified dates. Public repos need no sign-in; when signed in, the account's own private repos resolve too. An unknown or inaccessible repo is a clear error.

### How do I automatically get a model, dataset or Space on huggingface.co?

Ask an AI agent connected to Reduck to run reduck/huggingface.co/get_repo, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/huggingface.co/get_repo

### Is there a huggingface.co API to get a model, dataset or Space?

You do not need one. "Hugging Face — get a model, dataset or Space" drives the real huggingface.co pages in a browser, so it works whether or not huggingface.co offers an API for this.

### What information do I need to provide?

Required: id. Optional: type.

### What does it return?

It returns id, sdk, sha, url, tags, type, files, gated, likes, author, license, private, disabled, createdAt, downloads, libraryName, pipelineTag, lastModified, runtimeStage.

### Do I need to be logged in to huggingface.co?

No. It only uses pages of huggingface.co that are reachable without signing in.

### Does it change anything on huggingface.co, or only read data?

It only reads. It looks things up on huggingface.co and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/huggingface.co/get_repo, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/huggingface.co/get_repo

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/huggingface.co/get_repo
