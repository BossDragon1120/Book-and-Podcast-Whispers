---
name: podcast-whisper
description: Use when the user shares a dictated reflection on a podcast episode, usually M&A Science and usually raw Wispr Flow text. Turns it into an episode note in the Book-and-Podcast-Whispers repo, adds agent ideas to the backlog, and updates threads and the listening log.
---

# Podcast Whisper

Turn a quick spoken reflection on a podcast episode into an episode note, and capture any **agent ideas** it suggests.

## Inputs
- The raw dictation.
- The episode: title, link or guest. If the user gives only a guest or topic, find the episode page (for M&A Science: `mascience.com/podcast/...`) and confirm it with them.

## Steps
1. **Get the episode facts** (title, guest, role, company, URL) from the episode page, not from memory.
2. **Write the note** at `podcasts/<show>/<today>-<episode-slug>.md` from `templates/podcast-episode.md`. Put the raw dictation, unedited, in the collapsed "Raw dictation" block.
   - Use the user's ideas and voice; fix speech-to-text errors and cut repetition. Don't add opinions they didn't express.
   - **Agent ideas:** turn each pain the user mentions, plus any manual, repetitive or judgment-heavy task the guest described that the user reacted to, into a bullet in this form: pain → agent (inputs → output) → who uses it. Mark ideas that come from you rather than the user with *(suggested)*.
   - Paraphrase the episode. Quote at most once, under 15 words.
3. **Update `agent-ideas.md`.** Add one row per new idea, status 💡, with a link back to the note. If an idea is already there, add this episode as another source instead of adding a duplicate row.
4. **Update threads.** Add a dated entry to each related `threads/<theme>.md`, never rewriting earlier entries.
5. **Update `listening-log.md`.**
6. **Commit** with the message `Podcast: <Episode title> (<date>)`.
7. **Reply** with the agent ideas you added and the threads you touched.
