# Switch Trello account language

Automatically switch Trello account language on trello.com. Choose English, French, German, Italian or Spanish and get back the language Trello now loads in.

- Site: trello.com
- Address: `reduck/trello.com/switch_language`
- Updated: 2026-10-05 (v3)
- Author: Reduck AI (reduck)

## About

Trello's display language follows the Language preference on your Atlassian account. By hand, Trello's help pages give the path Account, Settings, Change Language, and Atlassian lists the setting under Account preferences, Language. This run opens the Language dropdown on id.atlassian.com and picks the entry written in its own language (Deutsch, Français, Español), so menus you cannot read are no obstacle. Then it reloads trello.com up to 15 times and returns the code the page loaded in, such as "fr" for French or "en-gb" for UK English, or stops with an error if Trello never catches up. A trainer putting together the French edition of a team's Trello onboarding guide would switch to fr_FR, grab the screenshots, then go back with en_GB. Only six locale codes are accepted. Jira and Confluence on the same account change too. The run also depends on the layout of Atlassian's preferences page, so a redesign there is what would break it first.

## Run it

Ask an AI agent connected to Reduck over MCP (`https://mcp.reduck.ai/mcp`) to run `reduck/trello.com/switch_language`, or run it from a terminal:

```bash
npx @reduck-ai/cli@latest run --script reduck/trello.com/switch_language
```

## Input

- `locale` (string, required): Locale code, e.g. "en_GB", "en_US", "fr_FR", "de_DE", "it_IT", "es_ES".

## Output

- `locale` (string, required)

## Example output

Shape only: placeholder values generated from the output schema, not a real run.

```json
{
  "locale": "…"
}
```

## FAQ

### What does "Switch Trello account language" do?

Change the display language of your Trello account, via Atlassian's account-level language preference. Pass a locale code (e.g. "en_GB", "fr_FR", "de_DE", "it_IT", "es_ES"). Returns the language now active in Trello.

### How do I automatically switch Trello account language on trello.com?

Ask an AI agent connected to Reduck to run reduck/trello.com/switch_language, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/trello.com/switch_language

### Is there a trello.com API to switch Trello account language?

You do not need one. "Switch Trello account language" drives the real trello.com pages in a browser, so it works whether or not trello.com offers an API for this.

### What information do I need to provide?

Required: locale.

### What does it return?

It returns locale.

### Do I need to be logged in to trello.com?

Yes. It acts as you on trello.com: on your own Chrome it reuses your session, and on a Reduck-hosted browser it loads the trello.com cookies saved by the Reduck extension.

### Does it change anything on trello.com, or only read data?

It makes changes on trello.com, like sending, posting, booking or buying something.

### How do I run it?

Ask an AI agent connected to Reduck to run reduck/trello.com/switch_language, or run it from a terminal with the Reduck CLI: npx @reduck-ai/cli@latest run --script reduck/trello.com/switch_language

### Who maintains it?

It is part of Reduck's official curated catalogue.

### Can it switch Trello to Portuguese, Japanese or other languages?

The Trello language switch accepts six locale codes: en_GB, en_US, fr_FR, de_DE, it_IT and es_ES. Anything else, such as pt_BR or ja_JP, stops with an "Unsupported locale" error before any page is opened, so your account is left as it was. Trello's help pages list 21 languages, which leaves 16, Portuguese and Japanese among them, to set by hand from Trello's own account settings.

### Will changing my Trello language also change Jira and Confluence?

Changing the language this way also changes Jira and Confluence on the same Atlassian account, because the preference belongs to the account rather than to Trello. If your Trello login is a different Atlassian account from the one you use for Jira at work, Jira stays as it was. Atlassian also says a language set on the account overrides whatever default your admin chose.

### Does it change the language of the Trello mobile app?

Switching the account language does not reach the Trello apps for iOS and Android, which follow your phone's system language and, when Trello lacks that one, the next preferred language on the phone that Trello supports. The change shows up in Trello on the web.

### How do I get Trello back to English if it is stuck in a language I cannot read?

To get Trello back to English, pass en_US or en_GB: the run looks for the entry labelled English (US) or English (UK) in the Atlassian Language dropdown, which keeps each language under its own name, so it does not matter which language the menus are stuck in. To do it by hand, open id.atlassian.com/manage-profile/account-preferences and look for those same two English labels in the Language list.

Source: https://reduck.ai/explore/scripts/reduck/trello.com/switch_language
