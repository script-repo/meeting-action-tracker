# Meeting Action Tracker

Grok Bot agent that watches Granola meeting notes, pulls out clear action items, and keeps them on a markdown kanban board.

## Live bot

- **Name:** Meeting Action Tracker
- **Agent id:** `e3610fce-939b-4590-81ff-1fcd6aa46197`
- **Owner GitHub:** [script-repo](https://github.com/script-repo)

## What it does

1. Checks Granola for new or updated meeting notes
2. Extracts real action items (owner, task, due date when present, source meeting)
3. Dedupes against the existing board
4. Writes new items into a markdown kanban (`Backlog` / `Doing` / `Done`)
5. Summarizes what changed; stays quiet on scheduled runs when nothing is new

## Repo layout

| Path | Purpose |
| --- | --- |
| `bots/meeting-action-tracker.md` | Publishable botdirectory-style prompt |
| `templates/action-board.md` | Starter markdown kanban |
| `AGENT.md` | Full operating instructions for the live bot |

## Setup

1. Create a Grok Bot named **Meeting Action Tracker** (or import the prompt from `bots/meeting-action-tracker.md`).
2. Connect **Granola**.
3. Copy `templates/action-board.md` into your notes vault (or wherever you want the board) and tell the bot that path on first run.
4. Optional: schedule a routine to sync after meetings (for example every few hours on weekdays).

## Defaults used for this create

- Public GitHub repo
- Markdown board (no Linear/Notion/etc. yet)
- No secrets or private customer detail in this repo
