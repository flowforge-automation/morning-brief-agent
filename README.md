# Morning Brief Agent

An automated daily briefing agent that combines Google Calendar events and Gmail unread count into a single, friendly summary — delivered automatically every morning, no manual checking required.

## What it does

- Reads calendar events for today and the next few days
- Checks the unread email count in Gmail
- Summarizes both into a short digest (with emojis) using Claude
- Handles empty calendar / empty inbox gracefully instead of leaving gaps
- Delivers automatically on a daily schedule — no manual trigger needed

See [`case-study-morning-brief.md`](./case-study-morning-brief.md) for the full write-up.

## Two implementations

- **Cowork version** — an AI agent set up as a reusable Skill with a scheduled task, adjustable through plain-language instructions
- **Zapier version** — a 6-step no-code automation: Schedule trigger → Date calculation → Find Calendar Events → Find Unread Email → Claude summarization → Send Email

## How it works

1. A daily schedule trigger fires automatically (e.g. every morning at 8:00)
2. The date range (today + N days) is calculated dynamically, so it always looks the right number of days ahead
3. Calendar events and unread email count are fetched
4. Claude summarizes both into a short, friendly brief
5. The brief is delivered (email, in the Zapier version)

## Tech Stack

- Claude Cowork (AI agent platform, Anthropic)
- Zapier: Schedule by Zapier, Google Calendar, Gmail, Anthropic (Claude)
- Google Calendar API, Gmail API

## Notes

- No API keys or credentials are stored in this repository
- Categories, schedule time, and format are fully customizable per client (e.g. add Slack, a task manager, or team calendars)

## License

MIT (or update as needed)
