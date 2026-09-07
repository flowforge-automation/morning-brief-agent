# Morning Brief Agent (Calendar + Email Summary)

## The Problem

Starting the day often means opening multiple apps just to get oriented — checking the calendar for what's coming up, then switching to email to see what needs attention. It's a small task repeated every single morning, and it adds friction before the real work even starts.

## The Solution

An automated agent that runs every morning and delivers a single, ready-to-read summary combining:

- **Calendar events** for today and the next few days
- **Unread email count**, with a note when nothing urgent is waiting

No manual checking required — the brief arrives on its own, in a short, friendly format.

Built two ways to show flexibility across platforms:

## Version 1: Claude Cowork (AI agent, no code)

Set up as a saved, reusable Skill inside Cowork, running on an automatic daily schedule. Best fit: users who want an AI assistant that can be easily adjusted through conversation (e.g. "also flag emails from my manager") without touching any configuration screens.

## Version 2: Zapier (no-code automation, no code)

A six-step automation: a daily schedule trigger calculates the date range, pulls matching calendar events and the unread email count, sends both to Claude for summarization, and emails the result. Best fit: users who want a visual, inspectable workflow that a team can view and maintain without AI-specific tooling.

## How It Works (both versions)

1. A scheduled trigger runs automatically every morning
2. The agent reads upcoming calendar events (today + next few days) and the current unread email count
3. Claude summarizes both into a short, friendly digest — handling the "nothing scheduled" and "inbox empty" cases gracefully instead of leaving blanks
4. The summary is delivered automatically (as a chat message in Cowork, or by email in the Zapier version)

## Result

- **Zero manual checking** — the information arrives before you look for it
- **Handles edge cases automatically** — an empty calendar or empty inbox produces a clear, reassuring message instead of an awkward gap
- **Fully automated end-to-end** — both versions run on their own schedule with no daily action required
- **Easy to extend** — additional sources (Slack, Trello, a task manager) can be added to the same digest

## Tech Stack

- Claude Cowork (AI agent platform, Anthropic) with a scheduled task
- Zapier (Schedule trigger, Google Calendar, Gmail, Anthropic (Claude), Gmail Send — 6-step workflow)
- Google Calendar API, Gmail API

## Availability

This pattern adapts to any daily briefing need — combining calendar, email, task lists, or team channels into one automatic morning digest, timed and formatted however the client prefers.

---
*Tired of opening five apps before 9am? This can run itself.*
