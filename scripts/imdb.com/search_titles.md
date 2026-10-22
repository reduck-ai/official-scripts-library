# Search IMDb titles with advanced filters

Automatically search IMDb titles with advanced filters on imdb.com. Searches IMDb's advanced title search and returns matching movies, series and episodes with their IMDb rating, vote count, Metascore, genres, runtime, certificate, release date and plot. Filters on title name, title type, genre, release date range, IMDb rating range, vote count, runtime, country, language, keyword and popularity rank, sorted by rating, votes, popularity, box office, runtime or year.

- Site: imdb.com
- Address: `reduck/imdb.com/search_titles`
- Updated: 2026-10-21 (v3)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/imdb.com/search_titles`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/imdb.com/search_titles
```

## Input

- `count` (integer, optional): How many results to return. IMDb caps a single search at 250 and offers no way to reach results beyond that, so narrow the filters rather than paginating. Defaults to 50.
- `query` (string, optional): Words that must appear in the title name, e.g. "matrix".
- `genres` (array, optional): IMDb genres to include, in IMDb's English spelling: Action, Adventure, Animation, Biography, Comedy, Crime, Documentary, Drama, Family, Fantasy, Film-Noir, Game-Show, History, Horror, Music, Musical, Mystery, News, Reality-TV, Romance, Sci-Fi, Short, Sport, Talk-Show, Thriller, War, Western. Excluding genres is not available.
- `sortBy` (string, optional): Field to sort on. Defaults to popularity.
- `keywords` (array, optional): IMDb plot keywords, e.g. ["dystopia","time-travel"].
- `maxVotes` (integer, optional): Maximum number of IMDb user votes.
- `minVotes` (integer, optional): Minimum number of IMDb user votes.
- `countries` (array, optional): Two-letter country codes of origin, e.g. ["US","FR"].
- `languages` (array, optional): Two-letter language codes, e.g. ["en","ja"].
- `sortOrder` (string, optional): Sort direction. Defaults to ascending for popularity, which puts the most popular first.
- `titleTypes` (array, optional): Kinds of title to include. Defaults to feature films.
- `includeAdult` (boolean, optional): Include adult titles, which IMDb hides by default.
- `userRatingMax` (number, optional): Highest IMDb rating to accept.
- `userRatingMin` (number, optional): Lowest IMDb rating to accept.
- `releaseDateEnd` (string, optional): Latest release date, as YYYY-MM-DD.
- `releaseDateStart` (string, optional): Earliest release date, as YYYY-MM-DD.
- `popularityRankMax` (integer, optional): Worst IMDb popularity rank to accept.
- `popularityRankMin` (integer, optional): Best IMDb popularity rank to accept, where 1 is the most popular title.
- `runtimeMaxMinutes` (integer, optional): Longest runtime to accept, in minutes.
- `runtimeMinMinutes` (integer, optional): Shortest runtime to accept, in minutes.

## Output

- `titles` (array, required)
- `searchUrl` (string, required)
- `totalResults` (integer, required): Total number of titles matching the filters on IMDb, which can exceed the number returned.
- `returnedResults` (integer, required)
- `language` (string | null, optional): Language IMDb rendered the page in, which is the language of the genres field.

## FAQ

### What does "Search IMDb titles with advanced filters" do?

Searches IMDb's advanced title search and returns matching movies, series and episodes with their IMDb rating, vote count, Metascore, genres, runtime, certificate, release date and plot. Filters on title name, title type, genre, release date range, IMDb rating range, vote count, runtime, country, language, keyword and popularity rank, sorted by rating, votes, popularity, box office, runtime or year.

### How do I automatically search IMDb titles with advanced filters on imdb.com?

Ask an AI agent connected to Reduck to run reduck/imdb.com/search_titles, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/imdb.com/search_titles

### Is there a imdb.com API to search IMDb titles with advanced filters?

You do not need one. "Search IMDb titles with advanced filters" drives the real imdb.com pages in a browser, so it works whether or not imdb.com offers an API for this.

### What information do I need to provide?

Optional: count, query, genres, sortBy, keywords, maxVotes, minVotes, countries, languages, sortOrder, titleTypes, includeAdult, userRatingMax, userRatingMin, releaseDateEnd, releaseDateStart, popularityRankMax, popularityRankMin, runtimeMaxMinutes, runtimeMinMinutes.

### What does it return?

It returns titles, language, searchUrl, totalResults, returnedResults.

### Do I need to be logged in to imdb.com?

No. It only uses pages of imdb.com that are reachable without signing in.

### Does it change anything on imdb.com, or only read data?

It only reads. It looks things up on imdb.com and changes nothing there.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/imdb.com/search_titles, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/imdb.com/search_titles

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/imdb.com/search_titles
