# Remove a place from a Google Maps list

Automatically remove a place from a Google Maps list on google.com. Remove one Google Maps place from one of your saved lists, such as Favorites, Want to go or a list you made. Give the place by its place id (from search_places or get_place) or by a query that names one place, and the list by its name. When several Google accounts are signed in on the browser, choose one by its index from mail.google.com/list_accounts; the default is the browser's first account. Returns the place's name, the email of the account it was removed for, and whether it was removed now or was not in that list, so running it twice changes nothing. The place stays in the account's other lists. A query that Maps answers with a list of places fails and asks for search_places. A list name the account does not have fails and names the lists it has. This undoes save_place.

- Site: google.com
- Address: `reduck/google.com/unsave_place`
- Updated: 2026-10-22 (v1)
- Author: Reduck AI (reduck)

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/google.com/unsave_place`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/google.com/unsave_place
```

## Input

- `list` (string, required): Name of the list. The built-in lists take their English names in every account language: Favorites, Want to go, Travel plans, Starred places. A list you made takes the name you gave it. Matched without regard to case.
- `query` (string, optional): Name and address of one place (e.g. 'Tapas 24, Carrer de la Diputació 269, Barcelona'). It works only when Maps opens it as one place.
- `account` (integer, optional): Which Google account signed in on this browser to act as, by its index from mail.google.com/list_accounts. 0 is the browser's default account.
- `placeId` (string, optional): Google place id (e.g. 'ChIJ...'), as search_places or get_place returns it. The preferred input.

## Output

- `list` (string, required): Name of the list, as Maps shows it.
- `name` (string, required): Name of the place, as Maps shows it.
- `status` (string, required): removed: taken out of the list now. not_saved: the place was not in that list and nothing changed.
- `account` (string | null, required): Email of the Google account the place was removed for. null when Maps did not show it.

## FAQ

### What does "Remove a place from a Google Maps list" do?

Remove one Google Maps place from one of your saved lists, such as Favorites, Want to go or a list you made. Give the place by its place id (from search_places or get_place) or by a query that names one place, and the list by its name. When several Google accounts are signed in on the browser, choose one by its index from mail.google.com/list_accounts; the default is the browser's first account. Returns the place's name, the email of the account it was removed for, and whether it was removed now or was not in that list, so running it twice changes nothing. The place stays in the account's other lists. A query that Maps answers with a list of places fails and asks for search_places. A list name the account does not have fails and names the lists it has. This undoes save_place.

### How do I automatically remove a place from a Google Maps list on google.com?

Ask an AI agent connected to Reduck to run reduck/google.com/unsave_place, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/google.com/unsave_place

### Is there a google.com API to remove a place from a Google Maps list?

You do not need one. "Remove a place from a Google Maps list" drives the real google.com pages in a browser, so it works whether or not google.com offers an API for this.

### What information do I need to provide?

Required: list. Optional: query, account, placeId.

### What does it return?

It returns list, name, status, account.

### Do I need to be logged in to google.com?

Yes. It acts as you on google.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the google.com cookies saved by the Reduck extension.

### Does it change anything on google.com, or only read data?

It makes changes on google.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/google.com/unsave_place, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/google.com/unsave_place

### Who maintains it?

It is part of Reduck's official curated catalogue.

Source: https://reduck.ai/explore/scripts/reduck/google.com/unsave_place
