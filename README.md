# 📖🎧 Book & Podcast Whispers

**One book a month. One M&A Science episode a day.** I speak my reflections out loud with [Wispr Flow](https://wisprflow.ai), and Claude turns each dictation into a written note. Over time, this repo becomes a record of **how my thinking changes**, plus a running list of ideas for **M&A and integration agents** taken from what practitioners actually do.

## Two rhythms

| | 📖 Books | 🎧 Podcasts |
|---|---|---|
| **How often** | One a month | One M&A Science episode a day |
| **Capture** | Margin notes, then a longer dictation | A 2-minute dictation right after listening |
| **Skill** | [`book-whisper`](skills/book-whisper/SKILL.md) | [`podcast-whisper`](skills/podcast-whisper/SKILL.md) |
| **Becomes** | `books/…/reflection.md` | `podcasts/ma-science/<date>-<episode>.md` |
| **Also feeds** | `threads/`, `reading-log.md` | `threads/`, [`agent-ideas.md`](agent-ideas.md), `listening-log.md` |

## How books work

```
 margin notes ─▶ 🎙️ dictate with Wispr Flow ─▶ book-whisper skill ─▶ this repo
 (paper)          (raw, unedited)               (Claude)             ├─ raw dictation, kept as-is
                                                                     ├─ reflection.md
                                                                     ├─ threads/ updated
                                                                     └─ reading-log row
```

1. **Read and mark up** the book as usual.
2. **Dictate.** Open the book's raw file (or a chat with Claude), put your cursor there and talk through your margin notes with Wispr Flow. Don't edit; ramble.
3. **Run the [`book-whisper`](skills/book-whisper/SKILL.md) skill.** It saves the raw dictation, writes the reflection, links it to earlier books, and adds to the thread for each idea it touches.

## Layout

```
podcasts/<show>/YYYY-MM-DD-<episode>.md   one note per episode (raw dictation kept inside)
agent-ideas.md          backlog of agent ideas, each linked to its source
listening-log.md        one row per episode
books/YYYY-MM-<book-slug>/
  raw/YYYY-MM-DD.md     dictations exactly as spoken, never edited
  reflection.md         the written reflection
threads/<theme>.md      one file per recurring idea, with a dated entry from each book
reading-log.md          one row per book
templates/              reflection.md, thread.md, podcast-episode.md
skills/                 book-whisper and podcast-whisper
```

## Why threads and agent ideas

A reflection captures one book or episode. A **thread** follows one idea across many books and episodes (leadership, change, how organizations learn…), with dated entries, so you can see a view form, get challenged, and shift. That's the evolution of thought.

The **agent ideas backlog** is the practical side. Every time a practitioner describes something slow, manual or full of judgment calls, it becomes a candidate agent. Each idea is linked to the episode or book it came from, so the reasoning behind it is easy to trace.

## Ground rules
- **My words, not the author's or the guest's.** Notes are my thinking. Quotes are short and rare, so this repo never stands in for the book or the episode.
- **Raw stays raw.** Dictations are kept unedited; only the reflection gets polished.
- **Changes of mind are recorded, not erased.** If a later book changes a view, the thread gets a new entry instead of having the old one rewritten.

## Connected to
[Little Panda Education](https://github.com/BossDragon1120/Little-Panda-Education): reflections and episode notes marked `status: done` include a `## Teachable moments` section that can become short videos.
