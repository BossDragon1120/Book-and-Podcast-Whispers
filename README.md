# 📖 Book Whispers

One book a month. I write in the margins as I read, then speak my reflections out loud with [Wispr Flow](https://wisprflow.ai). Claude turns each dictation into a written reflection, and over time this repo becomes a record of **how my thinking changes**, book by book.

## How it works

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
books/YYYY-MM-<book-slug>/
  raw/YYYY-MM-DD.md     dictations exactly as spoken, never edited
  reflection.md         the written reflection
threads/<theme>.md      one file per recurring idea, with a dated entry from each book
reading-log.md          one row per book
templates/              reflection.md and thread.md
skills/book-whisper/    the Claude skill that does the processing
```

## Why threads

A reflection captures one book. A **thread** follows one idea across many books (leadership, change, how organizations learn…), with dated entries, so you can see a view form, get challenged, and shift. That's the evolution of thought.

## Ground rules
- **My words, not the author's.** Reflections are my thinking. Quotes are short and rare, so this repo never stands in for the book.
- **Raw stays raw.** Dictations are kept unedited; only the reflection gets polished.
- **Changes of mind are recorded, not erased.** If a later book changes a view, the thread gets a new entry instead of having the old one rewritten.

## Connected to
[Little Panda Education](https://github.com/BossDragon1120/Little-Panda-Education): reflections marked `status: done` include a `## Teachable moments` section that can become short videos.
