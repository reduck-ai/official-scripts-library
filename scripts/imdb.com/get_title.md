# Get IMDb title details by IMDb ID

Automatically get IMDb title details by IMDb ID on imdb.com. Opens an IMDb title page and returns its details: IMDb rating and vote count, Metascore, popularity rank, genres, runtime, certificate, release date and country, plot summary, countries of origin, poster and trailer, plus the top billed directors, writers and stars with their IMDb name IDs.

- Site: imdb.com
- Address: `reduck/imdb.com/get_title`
- Updated: 2026-10-21 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/imdb.com/get_title`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/imdb.com/get_title
```

## Input

- `titleId` (string, required): IMDb title identifier, e.g. "tt0133093" for The Matrix.

## Output

- `url` (string, required)
- `titleId` (string, required): Identifier IMDb actually served, which can differ from the requested one when IMDb redirects a merged title.
- `plot` (string | null, optional)
- `title` (string | null, optional): Title as IMDb displays it, which can be a regional title that depends on where the browser is located (e.g. a French title from France). Use originalTitle for a value that does not vary.
- `genres` (array, optional): Genres in the page's language.
- `rating` (number | null, optional)
- `credits` (array, optional): Top billed credit groups as IMDb shows them, typically directors, writers and stars.
- `endYear` (integer | null, optional)
- `isAdult` (boolean | null, optional)
- `imageUrl` (string | null, optional)
- `language` (string | null, optional): Language IMDb rendered the page in, which is the language of the plot, genres and credit group fields.
- `metascore` (integer | null, optional)
- `titleType` (string | null, optional)
- `voteCount` (integer | null, optional)
- `trailerUrl` (string | null, optional)
- `certificate` (string | null, optional)
- `releaseDate` (string | null, optional): Release date as YYYY-MM-DD, when IMDb gives a full date.
- `releaseYear` (integer | null, optional)
- `originalTitle` (string | null, optional): Original title, independent of the page's language and the browser's region.
- `popularityRank` (integer | null, optional): Current IMDb popularity rank, where 1 is the most popular title.
- `releaseCountry` (string | null, optional): Country that release date refers to, which IMDb picks from the visitor's region.
- `runtimeMinutes` (integer | null, optional)
- `productionStage` (string | null, optional)
- `userReviewCount` (integer | null, optional)
- `requestedTitleId` (string, optional)
- `countriesOfOrigin` (array, optional)
- `criticReviewCount` (integer | null, optional)

## FAQ

### What does "Get IMDb title details by IMDb ID" do?

Opens an IMDb title page and returns its details: IMDb rating and vote count, Metascore, popularity rank, genres, runtime, certificate, release date and country, plot summary, countries of origin, poster and trailer, plus the top billed directors, writers and stars with their IMDb name IDs.

### How do I automatically get IMDb title details by IMDb ID on imdb.com?

Ask an AI agent connected to Reduck to run reduck/imdb.com/get_title, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/imdb.com/get_title

### Is there a imdb.com API to get IMDb title details by IMDb ID?

You do not need one. "Get IMDb title details by IMDb ID" drives the real imdb.com pages in a browser, so it works whether or not imdb.com offers an API for this.

### What information do I need to provide?

Required: titleId.

### What does it return?

It returns url, plot, title, genres, rating, credits, endYear, isAdult, titleId, imageUrl, language, metascore, titleType, voteCount, trailerUrl, certificate, releaseDate, releaseYear, originalTitle, popularityRank, releaseCountry, runtimeMinutes, productionStage, userReviewCount, requestedTitleId, countriesOfOrigin, criticReviewCount.

### Do I need to be logged in to imdb.com?

No. It only uses pages of imdb.com that are reachable without signing in.

### Does it change anything on imdb.com, or only read data?

It only reads. It looks things up on imdb.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/imdb.com/get_title, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/imdb.com/get_title

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/imdb.com/get_title
