---
name: book-whisper
description: Use when the user shares a dictated book reflection, usually raw Wispr Flow text, to turn it into a reflection in the Book-Whispers repo, update its idea threads and the reading log.
---

# Book Whisper

Turn a raw, spoken reflection on a book into a written reflection, and record how it moves the user's thinking over time.

## Inputs
- The raw dictation: rambling, unedited and often full of speech-to-text errors.
- The book title and author. Ask only if they can't be found in the dictation.

## Steps
1. **Save the raw text first.** Write it unchanged to `books/YYYY-MM-<book-slug>/raw/<today>.md`, under a one-line header naming the book and the date. Never edit raw files later.
2. **Read the history.** Read `reading-log.md`, the `threads/` that might relate, and any earlier reflection on this book.
3. **Write or update `reflection.md`** from `templates/reflection.md`:
   - Use the user's ideas and voice: first person, plain language. Fix speech-to-text errors and cut repetition, but don't add opinions they didn't express.
   - **What changed in my thinking:** state the before and after, and link the earlier books or threads it builds on or contradicts.
   - **Teachable moments:** 1–3 ideas that could each work as a 60–90 second video.
   - Quotes from the book: at most one or two, each under 15 words. Paraphrase everything else.
   - Leave `status: draft` unless the user says it's done.
4. **Update threads.** For each theme the reflection touches, add a dated entry to `threads/<theme>.md` (create it from `templates/thread.md` if it's new). Revise "Where I stand now" only if this book moved it. Never rewrite earlier entries.
5. **Update `reading-log.md`.** Add or update the book's row.
6. **Commit** with the message `Reflection: <Book Title> (<YYYY-MM>)`.
7. **Reply** with the reflection's "What changed in my thinking" section, the threads you updated, and a question if anything in the dictation was ambiguous.

## Rules
- Never put words in the user's mouth. If something is unclear, flag it; don't fill in the gap.
- Don't summarize the book beyond three sentences. This repo is about the user's thinking, not the book's contents.
